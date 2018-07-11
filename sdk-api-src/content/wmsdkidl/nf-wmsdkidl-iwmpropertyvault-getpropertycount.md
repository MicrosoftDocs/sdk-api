---
UID: NF:wmsdkidl.IWMPropertyVault.GetPropertyCount
title: IWMPropertyVault::GetPropertyCount
author: windows-sdk-content
description: The GetPropertyCount method retrieves a count of all the properties in the property vault.
old-location: wmformat\iwmpropertyvault_getpropertycount.htm
old-project: wmformat
ms.assetid: 2045183d-8683-416f-bda0-87c5fecf8c11
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: GetPropertyCount, GetPropertyCount method [windows Media Format], GetPropertyCount method [windows Media Format],IWMPropertyVault interface, IWMPropertyVault interface [windows Media Format],GetPropertyCount method, IWMPropertyVault.GetPropertyCount, IWMPropertyVault::GetPropertyCount, IWMPropertyVaultGetPropertyCount, wmformat.iwmpropertyvault_getpropertycount, wmsdkidl/IWMPropertyVault::GetPropertyCount
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
 - IWMPropertyVault.GetPropertyCount
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPropertyVault::GetPropertyCount


## -description



The <b>GetPropertyCount</b> method retrieves a count of all the properties in the property vault.




## -parameters




### -param pdwCount [out]

Pointer to a <b>DWORD</b> that will receive the property count.


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
pdwCount is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0e51a9be-afd4-430b-8339-f45e8f9a7d20">IWMPropertyVault Interface</a>
 

 

