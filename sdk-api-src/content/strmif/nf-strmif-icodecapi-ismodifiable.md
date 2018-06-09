---
UID: NF:strmif.ICodecAPI.IsModifiable
title: ICodecAPI::IsModifiable
author: windows-sdk-content
description: The IsModifiable method queries whether a codec property can be changed, given the codec's current configuration.
old-location: dshow\icodecapi_ismodifiable.htm
old-project: DirectShow
ms.assetid: 5f7c7f72-02f2-4840-aaa2-9d26fe564577
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: ICodecAPI interface [DirectShow],IsModifiable method, ICodecAPI.IsModifiable, ICodecAPI::IsModifiable, ICodecAPIIsModifiable, IsModifiable, IsModifiable method [DirectShow], IsModifiable method [DirectShow],ICodecAPI interface, dshow.icodecapi_ismodifiable, strmif/ICodecAPI::IsModifiable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps | UWP apps]
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - ICodecAPI.IsModifiable
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# ICodecAPI::IsModifiable


## -description



        The <b>IsModifiable</b> method queries whether a codec property can be changed, given the codec's current configuration.
      


## -parameters




### -param Api [in]

Pointer to a GUID that specifies the property. For a list of standard codec properties, see <a href="https://msdn.microsoft.com/5d527af7-07cf-42e2-99bb-d56c856cc1bc">Codec API Properties</a>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The value of this property cannot be changed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The value of this property can be changed.

</td>
</tr>
</table>
 




## -remarks




        Any errors besides those in the previous table indicate an inability to process the call.
      




## -see-also




<a href="https://msdn.microsoft.com/82085fd5-2d31-48a0-b2ef-0eede4de60c8">Codec API Reference</a>



<a href="https://msdn.microsoft.com/3d19152f-17a3-4576-a2a2-5b827d9ca8d1">Encoder API</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI</a>
 

 

