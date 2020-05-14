---
UID: NF:wmsdkidl.IWMPropertyVault.CopyPropertiesFrom
title: IWMPropertyVault::CopyPropertiesFrom (wmsdkidl.h)
description: The CopyPropertiesFrom method copies all of the properties from another property vault to this one.helpviewer_keywords: ["CopyPropertiesFrom","CopyPropertiesFrom method [windows Media Format]","CopyPropertiesFrom method [windows Media Format]","IWMPropertyVault interface","IWMPropertyVault interface [windows Media Format]","CopyPropertiesFrom method","IWMPropertyVault.CopyPropertiesFrom","IWMPropertyVault::CopyPropertiesFrom","IWMPropertyVaultCopyPropertiesFrom","wmformat.iwmpropertyvault_copypropertiesfrom","wmsdkidl/IWMPropertyVault::CopyPropertiesFrom"]
old-location: wmformat\iwmpropertyvault_copypropertiesfrom.htm
tech.root: wmformat
ms.assetid: 34708ff4-a416-4f2a-abeb-18b9c24c4e7c
ms.date: 12/05/2018
ms.keywords: CopyPropertiesFrom, CopyPropertiesFrom method [windows Media Format], CopyPropertiesFrom method [windows Media Format],IWMPropertyVault interface, IWMPropertyVault interface [windows Media Format],CopyPropertiesFrom method, IWMPropertyVault.CopyPropertiesFrom, IWMPropertyVault::CopyPropertiesFrom, IWMPropertyVaultCopyPropertiesFrom, wmformat.iwmpropertyvault_copypropertiesfrom, wmsdkidl/IWMPropertyVault::CopyPropertiesFrom
f1_keywords:
- wmsdkidl/IWMPropertyVault.CopyPropertiesFrom
dev_langs:
- c++
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
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
- IWMPropertyVault.CopyPropertiesFrom
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPropertyVault::CopyPropertiesFrom


## -description



The <b>CopyPropertiesFrom</b> method copies all of the properties from another property vault to this one.




## -parameters




### -param pIWMPropertyVault [in]

Pointer to an <b>IWMPropertyVault</b> interface.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method is unable to allocate memory needed to copy.

</td>
</tr>
</table>
 




## -remarks



Passing <b>NULL</b> as <i>pIWMPropertyVault</i> will result in unpredictable errors.

<b>CopyPropertiesFrom</b> makes calls to other methods of <b>IWMPropertyVault</b>. Because all of the data is coming from the objects themselves, no errors should be returned from the other methods. A return code that is not in the table indicates the corruption of data in the property vault from which you are copying.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault">IWMPropertyVault Interface</a>
 

 

