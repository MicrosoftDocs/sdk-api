---
UID: NF:strmif.ICodecAPI.GetAllSettings
title: ICodecAPI::GetAllSettings method
author: windows-driver-content
description: The GetAllSettings method gets the codec's current properties and writes them to a stream.
old-location: dshow\icodecapi_getallsettings.htm
old-project: DirectShow
ms.assetid: 45685033-73cc-4810-90f2-49343494641b
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetAllSettings method [DirectShow], GetAllSettings method [DirectShow], ICodecAPI interface, GetAllSettings,ICodecAPI.GetAllSettings, ICodecAPI, ICodecAPI interface [DirectShow], GetAllSettings method, ICodecAPI::GetAllSettings, ICodecAPIGetAllSettings, dshow.icodecapi_getallsettings, strmif/ICodecAPI::GetAllSettings
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
-	ICodecAPI.GetAllSettings
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# ICodecAPI::GetAllSettings method


## -description



The <b>GetAllSettings</b> method gets the codec's current properties and writes them to  a stream.




## -parameters




### -param __MIDL__ICodecAPI0000






#### - pStream [in]


            Pointer to the <b>IStream</b> interface of the stream.
          


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

To load the properties from the stream back onto the codec, call <a href="https://msdn.microsoft.com/1148e380-a4fc-4392-861e-8ea695060032">ICodecAPI::SetAllSettings</a> or <a href="https://msdn.microsoft.com/30f840d1-4c73-4a76-ba0b-c04f2901ad76">ICodecAPI::SetAllSettingsWithNotify</a>.

The format of the data that is written to the stream depends on the implementation of the codec. There is no standard serialization format.  An application should not attempt to save the properties from one codec and load them on a different codec.




## -see-also




<a href="https://msdn.microsoft.com/82085fd5-2d31-48a0-b2ef-0eede4de60c8">Codec API Reference</a>



<a href="https://msdn.microsoft.com/3d19152f-17a3-4576-a2a2-5b827d9ca8d1">Encoder API</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI</a>
 

 

