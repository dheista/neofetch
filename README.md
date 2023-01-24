# neofetch
Customizations of neofetch

add to the neofetch binary:

get_tbw() {
    tbw="$(/usr/local/bin/smartctl -ai disk0 | grep Written | cut -f2 -d\[ | cut -f1 -d\])"
}

Then add to the neofetch config:

    info "TBW:" tbw
