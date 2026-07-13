---
UID: NS:dsclient.DSBITEMW
title: DSBITEMW (dsclient.h)
description: Contains data about an item in the Active Directory container browser dialog box. (Unicode)
helpviewer_keywords: ["*PDSBITEMW","DSBF_DISPLAYNAME","DSBF_ICONLOCATION","DSBF_STATE","DSBITEM","DSBITEM structure [Active Directory]","DSBITEMA","DSBITEMW","DSBS_CHECKED","DSBS_HIDDEN","DSBS_ROOT","PDSBITEM","PDSBITEM structure pointer [Active Directory]","_glines_dsbitem","ad.dsbitem","dsclient/DSBITEM","dsclient/DSBITEMA","dsclient/DSBITEMW","dsclient/PDSBITEM"]
old-location: ad\dsbitem.htm
tech.root: ad
ms.assetid: 580b8aea-8411-41de-a2d9-1c3e3b35dd5a
ms.date: 12/05/2018
ms.keywords: '*PDSBITEMW, DSBF_DISPLAYNAME, DSBF_ICONLOCATION, DSBF_STATE, DSBITEM, DSBITEM structure [Active Directory], DSBITEMA, DSBITEMW, DSBS_CHECKED, DSBS_HIDDEN, DSBS_ROOT, PDSBITEM, PDSBITEM structure pointer [Active Directory], _glines_dsbitem, ad.dsbitem, dsclient/DSBITEM, dsclient/DSBITEMA, dsclient/DSBITEMW, dsclient/PDSBITEM'
req.header: dsclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DSBITEMW (Unicode) and DSBITEMA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DSBITEMW, *PDSBITEMW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PDSBITEMW
 - dsclient/PDSBITEMW
 - DSBITEMW
 - dsclient/DSBITEMW
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
 - DSBITEM
 - DSBITEMA
 - DSBITEMW
---

# DSBITEMW structure


## -description

The <b>DSBITEM</b> structure contains data about an item in the Active Directory container browser dialog box. This structure is passed with the <b>DSBM_QUERYINSERT</b> notification to the <a href="/windows/desktop/api/shlobj_core/nc-shlobj_core-bffcallback">BFFCallBack</a> callback function. The container browser dialog box is created with the <a href="/windows/desktop/api/dsclient/nf-dsclient-dsbrowseforcontainera">DsBrowseForContainer</a> function.

## -struct-fields

### -field cbStruct

Contains the size, in bytes, of the structure.

### -field pszADsPath

Pointer to a  null-terminated Unicode string that contains the ADsPath of the item.

### -field pszClass

Pointer to a null-terminated Unicode string that contains the object class name of the item.

### -field dwMask

Contains a set of flags that indicate which members of the structure contain valid data. This can be zero or a combination of one or more of the following values.



#### DSBF_DISPLAYNAME

The <b>szDisplayName</b> member contains valid data.



#### DSBF_ICONLOCATION

The <b>szIconLocation</b> and <b>iIconResID</b> members contain valid data.



#### DSBF_STATE

The <b>dwState</b> and <b>dwStateMask</b> members contain valid data.

### -field dwState

Contains a set of flags that indicate the state of the item. This can be zero or a combination of one or more of the following values.



#### DSBS_CHECKED

If this flag is set, the item is selected. Otherwise, the item is not selected. This flag is not currently supported.



#### DSBS_HIDDEN

If this flag is set, the item is hidden. Otherwise, the item is visible.



#### DSBS_ROOT

If this flag is set, the item is a root item. Otherwise, the item is not a root item.

### -field dwStateMask

Contains a set of flags that indicate which flags in the <b>dwState</b> member contain valid data. This can be zero or a combination of one or more of the following values. For example, if <b>dwStateMask</b> has the  <b>DSBS_HIDDEN</b> flag set and <b>dwState</b> does not have the <b>DSBS_HIDDEN</b> flag set, then the item is visible. If <b>dwStateMask</b> does not have the <b>DSBS_HIDDEN</b> flag set, then the <b>DSBS_HIDDEN</b> flag in <b>dwState</b> must be ignored.



#### DSBS_CHECKED

The <b>DSBS_CHECKED</b> flag in the <b>dwState</b> member contains valid data.



#### DSBS_HIDDEN

The <b>DSBS_HIDDEN</b> flag in the <b>dwState</b> member contains valid data.



#### DSBS_ROOT

The <b>DSBS_ROOT</b> flag in the <b>dwState</b> member contains valid data.

### -field szDisplayName

Pointer to a null-terminated string that contains the display name of the item. The display name of an item can be changed by copying the new display name into this member, setting the <b>DSBF_DISPLAYNAME</b> flag in the <b>dwMask</b> member, and returning a nonzero value from <a href="/windows/desktop/api/shlobj_core/nc-shlobj_core-bffcallback">BFFCallBack</a>.

### -field szIconLocation

Pointer to a null-terminated string that contains the name of an .exe, .dll, or .ico file that contains the icon to display for the item. This can be any file type that can be passed to the <a href="/windows/desktop/api/shellapi/nf-shellapi-extracticona">ExtractIcon</a> function. The index for this icon is specified in <b>iIconResID</b>. To modify the icon displayed for the item, copy the icon source file name into this member, set  <b>iIconResID</b> to the zero-based index of the icon, set the <b>DSBF_ICONLOCATION</b> flag in  the <b>dwMask</b> member, and return a nonzero value from <a href="/windows/desktop/api/shlobj_core/nc-shlobj_core-bffcallback">BFFCallBack</a>.

### -field iIconResID

Contains the zero-based index of the icon to display for the item.

<div class="alert"><b>Note</b>  This is not the resource identifier of the icon.</div>
<div> </div>

##### - dwMask.DSBF_DISPLAYNAME

The <b>szDisplayName</b> member contains valid data.


##### - dwMask.DSBF_ICONLOCATION

The <b>szIconLocation</b> and <b>iIconResID</b> members contain valid data.


##### - dwMask.DSBF_STATE

The <b>dwState</b> and <b>dwStateMask</b> members contain valid data.


##### - dwState.DSBS_CHECKED

If this flag is set, the item is selected. Otherwise, the item is not selected. This flag is not currently supported.


##### - dwState.DSBS_HIDDEN

If this flag is set, the item is hidden. Otherwise, the item is visible.


##### - dwState.DSBS_ROOT

If this flag is set, the item is a root item. Otherwise, the item is not a root item.


##### - dwStateMask.DSBS_CHECKED

The <b>DSBS_CHECKED</b> flag in the <b>dwState</b> member contains valid data.


##### - dwStateMask.DSBS_HIDDEN

The <b>DSBS_HIDDEN</b> flag in the <b>dwState</b> member contains valid data.


##### - dwStateMask.DSBS_ROOT

The <b>DSBS_ROOT</b> flag in the <b>dwState</b> member contains valid data.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nc-shlobj_core-bffcallback">BFFCallBack</a>



<a href="/windows/desktop/api/dsclient/nf-dsclient-dsbrowseforcontainera">DsBrowseForContainer</a>



<a href="/windows/desktop/api/shellapi/nf-shellapi-extracticona">ExtractIcon</a>

## -remarks

> [!NOTE]
> The dsclient.h header defines DSBITEM as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

