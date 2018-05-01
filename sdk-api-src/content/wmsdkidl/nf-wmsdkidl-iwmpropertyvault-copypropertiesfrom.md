---
UID: NF:wmsdkidl.IWMPropertyVault.CopyPropertiesFrom
title: IWMPropertyVault::CopyPropertiesFrom method
author: windows-driver-content
description: The CopyPropertiesFrom method copies all of the properties from another property vault to this one.
old-location: wmformat\iwmpropertyvault_copypropertiesfrom.htm
old-project: wmformat
ms.assetid: 34708ff4-a416-4f2a-abeb-18b9c24c4e7c
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: CopyPropertiesFrom method [windows Media Format], CopyPropertiesFrom method [windows Media Format], IWMPropertyVault interface, CopyPropertiesFrom,IWMPropertyVault.CopyPropertiesFrom, IWMPropertyVault, IWMPropertyVault interface [windows Media Format], CopyPropertiesFrom method, IWMPropertyVault::CopyPropertiesFrom, IWMPropertyVaultCopyPropertiesFrom, wmformat.iwmpropertyvault_copypropertiesfrom, wmsdkidl/IWMPropertyVault::CopyPropertiesFrom
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmvcore.lib
-	Wmvcore.dll
-	WMStubDRM.lib
-	WMStubDRM.dll
api_name:
-	IWMPropertyVault.CopyPropertiesFrom
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPropertyVault::CopyPropertiesFrom method


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




<a href="https://msdn.microsoft.com/0e51a9be-afd4-430b-8339-f45e8f9a7d20">IWMPropertyVault Interface</a>
 

 

