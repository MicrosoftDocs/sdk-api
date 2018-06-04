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

# IRichEditOle::GetObject


## -description


Retrieves information, stored in a <a href="https://msdn.microsoft.com/d7957c09-11aa-402e-9cff-3e3491059b08">REOBJECT</a> structure, about an object in a rich edit control.


## -parameters




### -param iob

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

Zero-based index that specifies which object to return information about. If this parameter is <b>REO_IOB_USE_CP</b>, information about the object at the character position specified by the <a href="https://msdn.microsoft.com/d7957c09-11aa-402e-9cff-3e3491059b08">REOBJECT</a> structure is returned.


### -param lpreobject

Type: <b><a href="https://msdn.microsoft.com/d7957c09-11aa-402e-9cff-3e3491059b08">REOBJECT</a>*</b>

Structure that receives information about the object. The reference count of the interfaces returned in this structure has been incremented; it is the responsibility of the caller to use the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> method to decrement the count.


### -param dwFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Operation flags that specify which interfaces to return in the structure. The <i>dwFlags</i> parameter can be a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="REO_GETOBJ_POLEOBJ"></a><a id="reo_getobj_poleobj"></a><dl>
<dt><b>REO_GETOBJ_POLEOBJ</b></dt>
</dl>
</td>
<td width="60%">
Get object interface.

</td>
</tr>
<tr>
<td width="40%"><a id="REO_GETOBJ_PSTG"></a><a id="reo_getobj_pstg"></a><dl>
<dt><b>REO_GETOBJ_PSTG</b></dt>
</dl>
</td>
<td width="60%">
Get storage interface.

</td>
</tr>
<tr>
<td width="40%"><a id="REO_GETOBJ_POLESITE"></a><a id="reo_getobj_polesite"></a><dl>
<dt><b>REO_GETOBJ_POLESITE</b></dt>
</dl>
</td>
<td width="60%">
Get site interface.

</td>
</tr>
<tr>
<td width="40%"><a id="REO_GETOBJ_NO_INTERFACES"></a><a id="reo_getobj_no_interfaces"></a><dl>
<dt><b>REO_GETOBJ_NO_INTERFACES</b></dt>
</dl>
</td>
<td width="60%">
Get no interfaces.

</td>
</tr>
<tr>
<td width="40%"><a id="REO_GETOBJ_ALL_INTERFACES"></a><a id="reo_getobj_all_interfaces"></a><dl>
<dt><b>REO_GETOBJ_ALL_INTERFACES</b></dt>
</dl>
</td>
<td width="60%">
Get all interfaces.

</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns <b>S_OK</b> if successful, or an error value otherwise. <b>E_INVALIDARG</b> is returned if no buffer for the <a href="https://msdn.microsoft.com/d7957c09-11aa-402e-9cff-3e3491059b08">REOBJECT</a> structure was given or if the <i>iob</i> value or character position is invalid.




## -see-also




<a href="https://msdn.microsoft.com/d6d1794b-f16c-4a8c-84f5-dfe8bd8be08c">IRichEditOle</a>



<a href="https://msdn.microsoft.com/d7957c09-11aa-402e-9cff-3e3491059b08">REOBJECT</a>



<b>Reference</b>
 

 

