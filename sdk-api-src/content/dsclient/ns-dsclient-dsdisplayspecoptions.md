---
UID: NS:dsclient._DSDISPLAYSPECOPTIONS
title: DSDISPLAYSPECOPTIONS (dsclient.h)
description: Used to supply data to a context menu or property page extension about the display specifiers used.
helpviewer_keywords: ["*LPDSDISPLAYSPECOPTIONS","*PDSDISPLAYSPECOPTIONS","DSDISPLAYSPECOPTIONS","DSDISPLAYSPECOPTIONS structure [Active Directory]","DSDSOF_DONTSIGNSEAL","DSDSOF_DSAVAILABLE","DSDSOF_HASUSERANDSERVERINFO","DSDSOF_SIMPLEAUTHENTICATE","LPDSDISPLAYSPECOPTIONS","LPDSDISPLAYSPECOPTIONS structure pointer [Active Directory]","PDSDISPLAYSPECOPTIONS","PDSDISPLAYSPECOPTIONS structure pointer [Active Directory]","_glines_dsdisplayspecoptions","ad.dsdisplayspecoptions","dsclient/DSDISPLAYSPECOPTIONS","dsclient/LPDSDISPLAYSPECOPTIONS","dsclient/PDSDISPLAYSPECOPTIONS"]
old-location: ad\dsdisplayspecoptions.htm
tech.root: ad
ms.assetid: 01b7a571-fdbd-41e9-96c9-843cc733a32c
ms.date: 12/05/2018
ms.keywords: '*LPDSDISPLAYSPECOPTIONS, *PDSDISPLAYSPECOPTIONS, DSDISPLAYSPECOPTIONS, DSDISPLAYSPECOPTIONS structure [Active Directory], DSDSOF_DONTSIGNSEAL, DSDSOF_DSAVAILABLE, DSDSOF_HASUSERANDSERVERINFO, DSDSOF_SIMPLEAUTHENTICATE, LPDSDISPLAYSPECOPTIONS, LPDSDISPLAYSPECOPTIONS structure pointer [Active Directory], PDSDISPLAYSPECOPTIONS, PDSDISPLAYSPECOPTIONS structure pointer [Active Directory], _glines_dsdisplayspecoptions, ad.dsdisplayspecoptions, dsclient/DSDISPLAYSPECOPTIONS, dsclient/LPDSDISPLAYSPECOPTIONS, dsclient/PDSDISPLAYSPECOPTIONS'
req.header: dsclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DSDISPLAYSPECOPTIONS, *PDSDISPLAYSPECOPTIONS, *LPDSDISPLAYSPECOPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DSDISPLAYSPECOPTIONS
 - dsclient/_DSDISPLAYSPECOPTIONS
 - PDSDISPLAYSPECOPTIONS
 - dsclient/PDSDISPLAYSPECOPTIONS
 - DSDISPLAYSPECOPTIONS
 - dsclient/DSDISPLAYSPECOPTIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dsclient.h
api_name:
 - DSDISPLAYSPECOPTIONS
---

# DSDISPLAYSPECOPTIONS structure


## -description

The <b>DSDISPLAYSPECOPTIONS</b> structure is returned by the <a href="/windows/desktop/AD/cfstr-ds-display-spec-options">CFSTR_DS_DISPLAY_SPEC_OPTIONS</a> clipboard format and is used to supply data to a context menu or property page extension about the display specifiers used. It is important to specify the credentials required by the extension, to access data in the Active Directory server.

## -struct-fields

### -field dwSize

The size of the structure for versioning purposes.

### -field dwFlags

A set of flags that indicate data about the object and define the contents of the structure. This can be zero or a combination of one or more of the following values.



#### DSDSOF_HASUSERANDSERVERINFO (0x00000001)

The <b>offsetUserName</b>, <b>offsetPassword</b>, <b>offsetServer</b> and <b>offsetServerConfigPath</b> members are valid.



#### DSDSOF_SIMPLEAUTHENTICATE (0x00000002)

Do not specify <b>ADS_SECURE_AUTHENTICATION</b> flag when calling <a href="/windows/desktop/api/adshlp/nf-adshlp-adsopenobject">ADsOpenObject</a>.



#### DSDSOF_DONTSIGNSEAL (0x00000004)

Do not sign and seal when opening directory service objects.



#### DSDSOF_DSAVAILABLE (0x40000000)

Forces the client to avoid checking if the user is authenticated, the network is present or logged in, assuming the client belongs to a domain controlled by Active Directory Domain Services.

### -field offsetAttribPrefix

Contains the offset, in bytes, from the start of the <b>DSDISPLAYSPECOPTIONS</b> structure to a NULL-terminated, Unicode string that contains the prefix of the display specifier that the created extension was obtained from. This string can be one of the following values.



#### "admin"

The extension was obtained from the <a href="/windows/desktop/ADSchema/a-adminpropertypages">adminPropertyPages</a> attribute.



#### "shell"

The extension was obtained from the <a href="/windows/desktop/ADSchema/a-shellpropertypages">shellPropertyPages</a> attribute.

The following example shows how to use this member.


```cpp
pwszAttribPrefix = (LPWSTR)((LPBYTE)pdos + 
    pdso->offsetAttribPrefix);

```

### -field offsetUserName

Contains the offset, in bytes, from the start of the <b>DSDISPLAYSPECOPTIONS</b> structure to a NULL-terminated, Unicode string that contains the name of the user used to authenticate the bind. This member is only valid if <b>dwFlags</b> contains the <b>DSDSOF_HASUSERANDSERVERINFO</b> flag. If this member contains zero, the user name is not included.

The following example shows how to use this member.


```cpp
pwszUserName = (LPWSTR)((LPBYTE)pdso + 
    pdso->offsetUserName);

```

### -field offsetPassword

Contains the offset, in bytes, from the start of the <b>DSDISPLAYSPECOPTIONS</b> structure to a NULL-terminated, Unicode string that contains the password used to authenticate the bind. This member is only valid if <b>dwFlags</b> contains the <b>DSDSOF_HASUSERANDSERVERINFO</b> flag. If this member contains zero, the password is not included.

The following example shows how to use this member.


```cpp
pwszPassword = (LPWSTR)((LPBYTE)pdso + 
    pdso->offsetPassword);

```

### -field offsetServer

Contains the offset, in bytes, from the start of the <b>DSDISPLAYSPECOPTIONS</b> structure to a NULL-terminated, Unicode string that contains the name of the server. This member is only valid if <b>dwFlags</b> contains the <b>DSDSOF_HASUSERANDSERVERINFO</b> flag. If this member contains zero, the server name is not included.

The following example shows how to use this member.


```cpp
pwszServer = (LPWSTR)((LPBYTE)pdso + 
    pdso->offsetServer);

```

### -field offsetServerConfigPath

Contains the offset, in bytes, from the start of the <b>DSDISPLAYSPECOPTIONS</b> structure to a NULL-terminated, Unicode string that contains the ADsPath of the server. This member is only valid if <b>dwFlags</b> contains the <b>DSDSOF_HASUSERANDSERVERINFO</b> flag. If this member contains zero, the server path is not included.

The following example shows how to use this member.


```cpp
pwszServerConfigPath = (LPWSTR)((LPBYTE)pdso + 
    pdso->offsetServerConfigPath);

```

## -see-also

<a href="/windows/desktop/api/adshlp/nf-adshlp-adsopenobject">ADsOpenObject</a>



<a href="/windows/desktop/AD/cfstr-ds-display-spec-options">CFSTR_DS_DISPLAY_SPEC_OPTIONS</a>



<a href="/windows/desktop/AD/display-structures-in-active-directory-domain-services">Display Structures in Active Directory Domain Services</a>