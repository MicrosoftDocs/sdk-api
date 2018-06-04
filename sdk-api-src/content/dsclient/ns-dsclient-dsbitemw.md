---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# DSBITEMW structure


## -description


The <b>DSBITEM</b> structure contains data about an item in the Active Directory container browser dialog box. This structure is passed with the <b>DSBM_QUERYINSERT</b> notification to the <a href="https://msdn.microsoft.com/91cfef29-3e0a-4dd0-be1a-215827c23143">BFFCallBack</a> callback function. The container browser dialog box is created with the <a href="https://msdn.microsoft.com/c95585b3-bf40-4aee-ae47-ca8f43daf0e6">DsBrowseForContainer</a> function.


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

Pointer to a null-terminated string that contains the display name of the item. The display name of an item can be changed by copying the new display name into this member, setting the <b>DSBF_DISPLAYNAME</b> flag in the <b>dwMask</b> member, and returning a nonzero value from <a href="https://msdn.microsoft.com/91cfef29-3e0a-4dd0-be1a-215827c23143">BFFCallBack</a>.


### -field szIconLocation

Pointer to a null-terminated string that contains the name of an .exe, .dll, or .ico file that contains the icon to display for the item. This can be any file type that can be passed to the <a href="_win32_extracticon_cpp">ExtractIcon</a> function. The index for this icon is specified in <b>iIconResID</b>. To modify the icon displayed for the item, copy the icon source file name into this member, set  <b>iIconResID</b> to the zero-based index of the icon, set the <b>DSBF_ICONLOCATION</b> flag in  the <b>dwMask</b> member, and return a nonzero value from <a href="https://msdn.microsoft.com/91cfef29-3e0a-4dd0-be1a-215827c23143">BFFCallBack</a>.


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




<a href="https://msdn.microsoft.com/91cfef29-3e0a-4dd0-be1a-215827c23143">BFFCallBack</a>



<a href="https://msdn.microsoft.com/c95585b3-bf40-4aee-ae47-ca8f43daf0e6">DsBrowseForContainer</a>



<a href="_win32_extracticon_cpp">ExtractIcon</a>
 

 

