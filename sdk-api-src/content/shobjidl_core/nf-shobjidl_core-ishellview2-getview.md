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

# IShellView2::GetView


## -description


Requests the current or default Shell view, together with all other valid view identifiers (VIDs) supported by this implementation of <a href="https://msdn.microsoft.com/a61aec39-406d-4066-941d-e788d64f4310">IShellView2</a>.


## -parameters




### -param pvid [out]

Type: <b>SHELLVIEWID*</b>

A pointer to the GUID of the requested view. The following views are defined in Shlguid.h.



#### VID_LargeIcons

{0057D0E0-3573-11CF-AE69-08002B2E1262}



#### VID_SmallIcons

{089000C0-3573-11CF-AE69-08002B2E1262}



#### VID_List

{0E1FA5E0-3573-11CF-AE69-08002B2E1262}



#### VID_Details

{137E7700-3573-11CF-AE69-08002B2E1262}



#### VID_Tile

{65F125E5-7BE1-4810-BA9D-D271C8432CE3}


### -param uView [in]

Type: <b>ULONG</b>

The type of view requested.



#### SV2GV_CURRENTVIEW

Current Shell view.



#### SV2GV_DEFAULTVIEW

Default Shell view.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a standard COM error code otherwise.




## -remarks



<b>IShellView2::GetView</b> retrieves a "viewset", which is the requested view (default or current) together with all other valid views for this instance of <a href="https://msdn.microsoft.com/a61aec39-406d-4066-941d-e788d64f4310">IShellView2</a>. Calling <b>IShellView2::GetView</b> with the <b>SV2GV_CURRENTVIEW</b> returns a GUID representing the current view and also iterates through the valid VIDs. This information is stored for later use in validating a new view before it is displayed.

The view can also be affected by other factors. A global user default VID and <a href="https://msdn.microsoft.com/16b92115-6e7d-41d3-960d-6783d779224c">view mode</a> is set  when the user presses the <b>Apply to All Folders</b> button in the <b>Folder Options</b> window. The VID is determined from <b>IShellView2::GetView</b> with the <b>SV2GV_CURRENTVIEW</b> flag
and  the view mode is determined from <a href="https://msdn.microsoft.com/69d18b4f-3a68-420c-a184-05c2f69a5ec6">GetCurrentInfo</a>. The view can also be affected by the persisted folder default. Windows Explorer saves the VID and view mode of a folder if the user has previously visited it. In some cases, the folder you are navigating from also can influence the view mode created for the new view that you are entering.

The priority of these assorted views can be generally said to be the following:

<ol>
<li>Persisted folder default</li>
<li>Global user default</li>
<li>Default view (SV2GV_DEFAULTVIEW)</li>
<li>Previous view</li>
</ol>
The priority of the previous view can be higher if the <b>Remember each folder's view settings</b> option is not selected in <b>Folder Options</b>. Other factors such as policies can also come into play, so the list above should be viewed only as a very broad guideline.



