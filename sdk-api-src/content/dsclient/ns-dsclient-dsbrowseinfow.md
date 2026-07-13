---
UID: NS:dsclient.DSBROWSEINFOW
title: DSBROWSEINFOW (dsclient.h)
description: The DSBROWSEINFO structure is used with the DsBrowseForContainer function to supply and return data about the Active Directory container browser dialog box. (Unicode)
helpviewer_keywords: ["*PDSBROWSEINFOW","DSBI_CHECKBOXES","DSBI_DONTSIGNSEAL","DSBI_ENTIREDIRECTORY","DSBI_EXPANDONOPEN","DSBI_HASCREDENTIALS","DSBI_IGNORETREATASLEAF","DSBI_INCLUDEHIDDEN","DSBI_NOBUTTONS","DSBI_NOLINES","DSBI_NOLINESATROOT","DSBI_NOROOT","DSBI_RETURNOBJECTCLASS","DSBI_RETURN_FORMAT","DSBI_SIMPLEAUTHENTICATE","DSBROWSEINFO","DSBROWSEINFO structure [Active Directory]","DSBROWSEINFOA","DSBROWSEINFOW","DSBROWSEINFOW structure [Active Directory]","PDSBROWSEINFOW","PDSBROWSEINFOW structure pointer [Active Directory]","_glines_dsbrowseinfo","ad.dsbrowseinfo","dsclient/DSBROWSEINFO","dsclient/DSBROWSEINFOA","dsclient/DSBROWSEINFOW","dsclient/PDSBROWSEINFOW"]
old-location: ad\dsbrowseinfo.htm
tech.root: ad
ms.assetid: eaa2da41-1ddf-42d3-b721-6649ad49acf1
ms.date: 12/05/2018
ms.keywords: '*PDSBROWSEINFOW, DSBI_CHECKBOXES, DSBI_DONTSIGNSEAL, DSBI_ENTIREDIRECTORY, DSBI_EXPANDONOPEN, DSBI_HASCREDENTIALS, DSBI_IGNORETREATASLEAF, DSBI_INCLUDEHIDDEN, DSBI_NOBUTTONS, DSBI_NOLINES, DSBI_NOLINESATROOT, DSBI_NOROOT, DSBI_RETURNOBJECTCLASS, DSBI_RETURN_FORMAT, DSBI_SIMPLEAUTHENTICATE, DSBROWSEINFO, DSBROWSEINFO structure [Active Directory], DSBROWSEINFOA, DSBROWSEINFOW, DSBROWSEINFOW structure [Active Directory], PDSBROWSEINFOW, PDSBROWSEINFOW structure pointer [Active Directory], _glines_dsbrowseinfo, ad.dsbrowseinfo, dsclient/DSBROWSEINFO, dsclient/DSBROWSEINFOA, dsclient/DSBROWSEINFOW, dsclient/PDSBROWSEINFOW'
req.header: dsclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DSBROWSEINFOW (Unicode) and DSBROWSEINFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DSBROWSEINFOW, *PDSBROWSEINFOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PDSBROWSEINFOW
 - dsclient/PDSBROWSEINFOW
 - DSBROWSEINFOW
 - dsclient/DSBROWSEINFOW
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
 - DSBROWSEINFOW
 - DSBROWSEINFOA
 - DSBROWSEINFOW
---

# DSBROWSEINFOW structure


## -description

The <b>DSBROWSEINFO</b> structure is used with the 
<a href="/windows/desktop/api/dsclient/nf-dsclient-dsbrowseforcontainera">DsBrowseForContainer</a> function to supply and return data about the Active Directory container browser dialog box.

## -struct-fields

### -field cbStruct

Contains the size, in bytes, of the <b>DSBROWSEINFO</b> structure. This is used by the <a href="/windows/desktop/api/dsclient/nf-dsclient-dsbrowseforcontainera">DsBrowseForContainer</a> function for versioning purposes.

### -field hwndOwner

Handle of the window used as the parent of the container browser dialog box.

### -field pszCaption

Pointer to a null-terminated string that contains the caption of the dialog box. If this member is <b>NULL</b>, a default caption is used.

### -field pszTitle

Pointer to a null-terminated string that contains additional text to be displayed in the dialog box above the tree control. If this member is <b>NULL</b>, no additional text is displayed.

### -field pszRoot

Pointer to a null-terminated Unicode string that contains the ADsPath of the container placed at the root of the dialog box. The user cannot navigate above this level using the dialog box.

### -field pszPath

Pointer to a null-terminated Unicode string that receives the ADsPath of the container selected in the dialog. This string will always be null-terminated even if <b>cchPath</b> is not large enough to hold the entire path. If <b>dwFlags</b> contains the <b>DSBI_EXPANDONOPEN</b> flag, this member contains the ADsPath of the container that should be initially selected in the dialog box.

### -field cchPath

Contains the size, in <b>WCHAR</b> characters, of the <b>pszPath</b> buffer.

### -field dwFlags

Contains a set of flags that define the behavior of the dialog box. This can be zero or a combination of one or more of the following values.



#### DSBI_NOBUTTONS (1 (0x1))

The <b>+</b> and <b>-</b> buttons are not displayed in the dialog box.



#### DSBI_NOLINES (2 (0x2))

The lines that connect the objects in the dialog box are not displayed.



#### DSBI_NOLINESATROOT (4 (0x4))

The lines and buttons above the root objects are not displayed.



#### DSBI_CHECKBOXES (256 (0x100))

Causes a check box to be placed next to each item in the tree. The user can use the mouse to select and clear this check box. This currently has limited usage because there is no way to set or get the check state of an item.



#### DSBI_NOROOT (65536 (0x10000))

The root object, specified by <b>pszRoot</b>, is not displayed and the immediate child objects of the root are displayed at the root of the tree. This flag has no effect if <b>pszRoot</b> is <b>NULL</b> or if this member contains <b>DSBI_ENTIREDIRECTORY</b>.



#### DSBI_INCLUDEHIDDEN (131072 (0x20000))

Include hidden objects in the dialog box.



#### DSBI_EXPANDONOPEN (262144 (0x40000))

When  the dialog box opens, the container specified in <b>pszPath</b> will be visible and selected.



#### DSBI_ENTIREDIRECTORY (589824 (0x90000))

Includes all the trusted domains to the server specified in <b>pszRoot</b> or, by default, the domain that the user is logged in to.



#### DSBI_RETURN_FORMAT (1048576 (0x100000))

Indicates that the <b>dwReturnFormat</b> member is valid. If this flag is not set, the path format defaults to X.500.



#### DSBI_HASCREDENTIALS (2097152 (0x200000))

<b>pUserName</b> and <b>pPassword</b> are used for the access credentials. Otherwise, if this member does not contain <b>DSBI_SIMPLEAUTHENTICATE</b>, the dialog uses the security context of the calling thread.



#### DSBI_IGNORETREATASLEAF (4194304 (0x400000))

When determining if the object is displayed in the dialog box, the <b>treatAsLeaf</b> display specifier is ignored.



#### DSBI_SIMPLEAUTHENTICATE (8388608 (0x800000))

Indicates that secure authentication is not required when calling <a href="/windows/desktop/api/adshlp/nf-adshlp-adsopenobject">ADsOpenObject</a>.



#### DSBI_RETURNOBJECTCLASS (16777216 (0x1000000))

Indicates that the <b>pszObjectClass</b> and <b>cchObjectClass</b> are valid and should be filled.



#### DSBI_DONTSIGNSEAL (33554432 (0x2000000))

Indicates that signing and sealing will not be used when communicating with the directory service.

### -field pfnCallback

Pointer to an application-defined  <a href="/windows/desktop/api/shlobj_core/nc-shlobj_core-bffcallback">BFFCallBack</a> callback function that receives notifications from the container browser dialog box. Set this member to <b>NULL</b> if it is not used.

### -field lParam

Contains an application-defined 32-bit value passed as the <i>lpData</i> parameter in all calls to <b>pfnCallback</b>. This member is ignored if <b>pfnCallback</b> is <b>NULL</b>.

### -field dwReturnFormat

Contains one of the <a href="/windows/win32/api/iads/ne-iads-ads_format_enum">ADS_FORMAT_ENUM</a> values that specifies the format that the ADSI path returned in <b>pszPath</b> will accept.

### -field pUserName

Pointer to a Unicode string that contains the user name used for the credentials. This member is ignored if <b>dwFlags</b> does not have the <b>DSBI_HASCREDENTIALS</b> flag set. If this member is <b>NULL</b>, the currently logged on  user name is used.

### -field pPassword

Pointer to a Unicode string that contains the password used for the credentials. This member is ignored if <b>dwFlags</b> does not have the <b>DSBI_HASCREDENTIALS</b> flag set. If this member is <b>NULL</b>, the password of the currently logged on user is used.

### -field pszObjectClass

Pointer to a Unicode string buffer that receives the class string of the selected. This member is ignored if <b>dwFlags</b> does not have the <b>DSBI_RETURNOBJECTCLASS</b> flag set.

### -field cchObjectClass

Contains the size, in <b>WCHAR</b> characters, of the <b>pszObjectClass</b> buffer.


##### - dwFlags.DSBI_CHECKBOXES (256 (0x100))

Causes a check box to be placed next to each item in the tree. The user can use the mouse to select and clear this check box. This currently has limited usage because there is no way to set or get the check state of an item.


##### - dwFlags.DSBI_DONTSIGNSEAL (33554432 (0x2000000))

Indicates that signing and sealing will not be used when communicating with the directory service.


##### - dwFlags.DSBI_ENTIREDIRECTORY (589824 (0x90000))

Includes all the trusted domains to the server specified in <b>pszRoot</b> or, by default, the domain that the user is logged in to.


##### - dwFlags.DSBI_EXPANDONOPEN (262144 (0x40000))

When  the dialog box opens, the container specified in <b>pszPath</b> will be visible and selected.


##### - dwFlags.DSBI_HASCREDENTIALS (2097152 (0x200000))

<b>pUserName</b> and <b>pPassword</b> are used for the access credentials. Otherwise, if this member does not contain <b>DSBI_SIMPLEAUTHENTICATE</b>, the dialog uses the security context of the calling thread.


##### - dwFlags.DSBI_IGNORETREATASLEAF (4194304 (0x400000))

When determining if the object is displayed in the dialog box, the <b>treatAsLeaf</b> display specifier is ignored.


##### - dwFlags.DSBI_INCLUDEHIDDEN (131072 (0x20000))

Include hidden objects in the dialog box.


##### - dwFlags.DSBI_NOBUTTONS (1 (0x1))

The <b>+</b> and <b>-</b> buttons are not displayed in the dialog box.


##### - dwFlags.DSBI_NOLINES (2 (0x2))

The lines that connect the objects in the dialog box are not displayed.


##### - dwFlags.DSBI_NOLINESATROOT (4 (0x4))

The lines and buttons above the root objects are not displayed.


##### - dwFlags.DSBI_NOROOT (65536 (0x10000))

The root object, specified by <b>pszRoot</b>, is not displayed and the immediate child objects of the root are displayed at the root of the tree. This flag has no effect if <b>pszRoot</b> is <b>NULL</b> or if this member contains <b>DSBI_ENTIREDIRECTORY</b>.


##### - dwFlags.DSBI_RETURNOBJECTCLASS (16777216 (0x1000000))

Indicates that the <b>pszObjectClass</b> and <b>cchObjectClass</b> are valid and should be filled.


##### - dwFlags.DSBI_RETURN_FORMAT (1048576 (0x100000))

Indicates that the <b>dwReturnFormat</b> member is valid. If this flag is not set, the path format defaults to X.500.


##### - dwFlags.DSBI_SIMPLEAUTHENTICATE (8388608 (0x800000))

Indicates that secure authentication is not required when calling <a href="/windows/desktop/api/adshlp/nf-adshlp-adsopenobject">ADsOpenObject</a>.

## -see-also

<a href="/windows/win32/api/iads/ne-iads-ads_format_enum">ADS_FORMAT_ENUM</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-adsopenobject">ADsOpenObject</a>



<a href="/windows/desktop/api/shlobj_core/nc-shlobj_core-bffcallback">BFFCallBack</a>



<a href="/windows/desktop/api/dsclient/nf-dsclient-dsbrowseforcontainera">DsBrowseForContainer</a>

## -remarks

> [!NOTE]
> The dsclient.h header defines DSBROWSEINFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

