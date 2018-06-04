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

# NPSearchDialog function


## -description


Enables network vendors to supply their own form of browsing and search, beyond the hierarchical view presented in the <b>Connection</b> dialog box. If a network provider supports this function, the <b>Connection</b> dialog box will enable the <b>Search</b> button when the selected item belongs to that provider. If the user hits the <b>Search</b> button, the <b>Connection</b> dialog box calls <b>NPSearchDialog</b> to handle the user request.


## -parameters




### -param hwndParent

TBD


### -param lpNetResource [in]

Pointer to the currently selected item in the <b>Network Connections</b> dialog box. A provider may choose to ignore this field.


### -param lpBuffer [out]

Pointer to a buffer that will receive the result of the search.


### -param cbBuffer [out]

<b>DWORD</b> that will specify the size of the buffer passed in.


### -param lpnFlags [in]

Pointer to a <b>DWORD</b> of flags that the provider can set to force certain actions after the dialog box is dismissed. The only flag supported is WNSRCH_REFRESH_FIRST_LEVEL, which forces MPR to collapse then expand and refresh the first level below this provider after the dialog box is dismissed.


#### - hParent [in]

Handle of the window to be used as the parent window of the dialog box.


## -returns



If the function succeeds and the user has clicked <b>OK</b>, <b>NPSearchDialog</b> should return WN_SUCCESS. Otherwise, it should return an error value, which can be one of the following. All other errors should be handled or reported directly by the provider's dialog box.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_CANCEL</b></dt>
</dl>
</td>
<td width="60%">
The user canceled the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The input buffer is too small.

</td>
</tr>
</table>
 




## -remarks



If the provider does not support enumeration, then the action associated with double-clicking the provider's entry will be to invoke its <b>Search</b> dialog box.



