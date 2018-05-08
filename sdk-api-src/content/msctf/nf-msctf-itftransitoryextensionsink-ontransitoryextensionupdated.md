---
UID: NF:msctf.ITfTransitoryExtensionSink.OnTransitoryExtensionUpdated
title: ITfTransitoryExtensionSink::OnTransitoryExtensionUpdated
author: windows-driver-content
description: ITfTransitoryExtensionSink::OnTransitoryExtensionUpdated method
old-location: tsf\itftransitoryextensionsink_ontransitoryextensionupdated.htm
old-project: TSF
ms.assetid: 2501e0b7-a1fe-46ee-8b18-b13de875d66b
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITfTransitoryExtensionSink interface [Text Services Framework],OnTransitoryExtensionUpdated method, ITfTransitoryExtensionSink.OnTransitoryExtensionUpdated, ITfTransitoryExtensionSink::OnTransitoryExtensionUpdated, OnTransitoryExtensionUpdated, OnTransitoryExtensionUpdated method [Text Services Framework], OnTransitoryExtensionUpdated method [Text Services Framework],ITfTransitoryExtensionSink interface, msctf/ITfTransitoryExtensionSink::OnTransitoryExtensionUpdated, tsf.itftransitoryextensionsink_ontransitoryextensionupdated
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msctf.dll
api_name:
-	ITfTransitoryExtensionSink.OnTransitoryExtensionUpdated
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfTransitoryExtensionSink::OnTransitoryExtensionUpdated


## -description




## -parameters




### -param pic [in]

[in] A pointer of <a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext</a> interface. This is a context object in which the update happened.


### -param ecReadOnly [in]

[in] A read only edit cookie to access the <i>pic</i>. Using this edit cookie, the application can get the text that is contained in the context object.


### -param pResultRange [in]

[in] A pointer of the <a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a> interface. This is the range of the result string (determined string).


### -param pCompositionRange [in]

[in] A pointer of the <a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a> interface. This is the range of the current composition string.


### -param pfDeleteResultRange [out]

[out] A pointer to return the bool value. If it is true, TSF manager deletes the result range so only the current composition range remains in the transitory extension.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 



