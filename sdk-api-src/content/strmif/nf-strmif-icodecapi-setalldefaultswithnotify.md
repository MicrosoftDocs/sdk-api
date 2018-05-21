---
UID: NF:strmif.ICodecAPI.SetAllDefaultsWithNotify
title: ICodecAPI::SetAllDefaultsWithNotify
author: windows-driver-content
description: The SetAllDefaultsWithNotify method resets all codec properties to their default values, and returns a list of the properties that changed.
old-location: dshow\icodecapi_setalldefaultswithnotify.htm
old-project: DirectShow
ms.assetid: 5f35845f-db62-466a-86cd-5788cdaa9809
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: ICodecAPI interface [DirectShow],SetAllDefaultsWithNotify method, ICodecAPI.SetAllDefaultsWithNotify, ICodecAPI::SetAllDefaultsWithNotify, ICodecAPISetAllDefaultsWithNotify, SetAllDefaultsWithNotify, SetAllDefaultsWithNotify method [DirectShow], SetAllDefaultsWithNotify method [DirectShow],ICodecAPI interface, dshow.icodecapi_setalldefaultswithnotify, strmif/ICodecAPI::SetAllDefaultsWithNotify
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	ICodecAPI.SetAllDefaultsWithNotify
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# ICodecAPI::SetAllDefaultsWithNotify


## -description



        The <b>SetAllDefaultsWithNotify</b> method resets all codec properties to their default values, and returns a list of the properties that changed.
      


## -parameters




### -param ChangedParam [out]


            Receives a pointer to an array of GUIDs. The array contains the GUIDs of any properties that changed as a result of this method call. The caller must free the array by calling <b>CoTaskMemFree</b>.
          


### -param ChangedParamCount [out]


            Receives the number of elements in the <i>ChangedParam</i> array.
          


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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
</table>
 




## -remarks



Codecs that implement <a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI</a> are  not required to support this method.




## -see-also




<a href="https://msdn.microsoft.com/82085fd5-2d31-48a0-b2ef-0eede4de60c8">Codec API Reference</a>



<a href="https://msdn.microsoft.com/3d19152f-17a3-4576-a2a2-5b827d9ca8d1">Encoder API</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI</a>



<a href="https://msdn.microsoft.com/863ba518-c3c6-47d8-96d8-445a7e4d02aa">ICodecAPI::GetValue</a>
 

 

