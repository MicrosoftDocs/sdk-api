---
UID: NF:wmsdkidl.IWMPropertyVault.GetPropertyByName
title: IWMPropertyVault::GetPropertyByName
author: windows-sdk-content
description: The GetPropertyByName method retrieves a property from the vault by its name.
old-location: wmformat\iwmpropertyvault_getpropertybyname.htm
old-project: wmformat
ms.assetid: 65740366-ac0a-4d18-9f61-a79670998e6a
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetPropertyByName, GetPropertyByName method [windows Media Format], GetPropertyByName method [windows Media Format],IWMPropertyVault interface, IWMPropertyVault interface [windows Media Format],GetPropertyByName method, IWMPropertyVault.GetPropertyByName, IWMPropertyVault::GetPropertyByName, IWMPropertyVaultGetPropertyByName, wmformat.iwmpropertyvault_getpropertybyname, wmsdkidl/IWMPropertyVault::GetPropertyByName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WM_AETYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMPropertyVault.GetPropertyByName
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPropertyVault::GetPropertyByName


## -description



The <b>GetPropertyByName</b> method retrieves a property from the vault by its name.




## -parameters




### -param pszName [in]

Pointer to a <b>null</b>-terminated string containing the name of the property to be retrieved.


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
<i>pszName</i> or <i>pdwSize</i> or <i>pType</i> is <b>NULL</b>.

OR

<i>pszName</i> contains an invalid property name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ASF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
<i>pdwSize</i> specifies a size for <i>pValue</i> that is not large enough to hold the data.

</td>
</tr>
</table>
 




## -remarks



You must make two calls to <b>GetPropertyByName</b> to properly retrieve the value of the property. On the first call, pass <b>NULL</b> for <i>pValue</i>. When the call returns, <i>pdwSize</i> will point to the correct sizes of the buffer. Then on the second call, pass a properly sized buffer as <i>pValue</i> to receive the data.




## -see-also




<a href="https://msdn.microsoft.com/0e51a9be-afd4-430b-8339-f45e8f9a7d20">IWMPropertyVault Interface</a>



<a href="https://msdn.microsoft.com/edecc6d2-f784-4205-bd79-6098e553d5cd">IWMPropertyVault::GetPropertyByIndex</a>



<a href="https://msdn.microsoft.com/0fae0ecf-efa9-46d0-8324-4065f351291e">IWMPropertyVault::SetProperty</a>
 

 

