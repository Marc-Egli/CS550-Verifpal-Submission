# CS550 Project - Formal verification of Kerberos with Veripal

### Repository structure
``` 
.
├── models
│   ├── kerberos_active_guarded.vp
│   ├── kerberos_active.vp
│   ├── kerberos_oracle.vp
│   └── kerberos_passive.vp
├── outputs
│   ├── oracle_colored.log
│   └── oracle_uncolored.log
└── README.md
``` 

The models folders contains the different Verifpal implementations of Kerberos.
- `kerberos_active_guarded.vp`: active attacker, all variables guarded. Verification terminates in 20 minutes.
- `kerberos_active.vp`: active attacker, all variable unguarded. Verification takes weeks/months.
- `kerberos_oracle.vp`: active attacker with a chosen plaintext oracle. An attack is found after a few hours
- `kerberos_passive.vp`: passive attacker. Verification terminates in a few seconds.

In `outputs` you find the Verifpal verification trace obtained by running the verification of `kerberos_oracle.vp`
for a few hours, this contains the Proof of Concept of the found attack.

### Running Verifpal

Follow the [official documentation](https://verifpal.com/software/) to install Verifpal.

Once done that, you can run Verifpal as follows:
```
./verifpal verify <model_to_verify>
```

### Authors

- Bétrisey Samuel (282163)
- Egli Marc (283231)
- Romerio Lucio (249936)
