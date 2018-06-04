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

# IWMPropertyVault::GetPropertyByIndex


## -description



The <b>GetPropertyByIndex</b> method retrieves a property from the vault by its index value.




## -parameters




### -param dwIndex [in]

<b>DWORD</b> containing the property index.


### -param pszName [out]

Pointer to a wide-character <b>null</b>-terminated string containing the name of the property.


### -param pdwNameLen [in, out]

On input, a pointer to a <b>DWORD</b> containing the length, in wide characters, of the string at <i>pszName</i>. On output, specifies the number of characters, including the terminating <b>null</b> character, required to hold the property name.


### -param pType [out]

Pointer to a member of the <a href="https://msdn.microsoft.com/2a2756f9-2d76-48c9-bbea-35ee33a39918">WMT_ATTR_DATATYPE</a> enumeration type. This parameter specifies the type of data pointed to by <i>pValue</i>.


### -param pValue [out]

Pointer to a data buffer containing the value of the property. This value can be one of several types. The type of data that the buffer contains on output is specified by the value of <i>pType</i>.


### -param pdwSize [in, out]

Pointer to a <b>DWORD</b> containing the size, in bytes, of the data at <i>pValue</i>.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pdwNameLen</i> or <i>pdwSize</i> or <i>pType</i> is <b>NULL</b>.

OR

The index specified is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ASF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
One of the buffers (<i>pszName</i> or <i>pValue</i>) is not big enough to hold the property information.

</td>
</tr>
</table>
 




## -remarks



You must make two calls to <b>GetPropertyByIndex</b> to properly retrieve all of the information. On the first call, pass <b>NULL</b> for both <i>pszName</i> and <i>pValue</i>. When the call returns, <i>pdwNameLen</i> and <i>pdwSize</i> point to the correct sizes of their respective buffers. Then on the second call, pass properly sized buffers as <i>pszName</i> and <i>pValue</i> to receive the data.




## -see-also




<a href="https://msdn.microsoft.com/0e51a9be-afd4-430b-8339-f45e8f9a7d20">IWMPropertyVault Interface</a>



<a href="https://msdn.microsoft.com/65740366-ac0a-4d18-9f61-a79670998e6a">IWMPropertyVault::GetPropertyByName</a>



<a href="https://msdn.microsoft.com/0fae0ecf-efa9-46d0-8324-4065f351291e">IWMPropertyVault::SetProperty</a>
 

 

