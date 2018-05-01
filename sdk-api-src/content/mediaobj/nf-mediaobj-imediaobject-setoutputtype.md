---
UID: NF:mediaobj.IMediaObject.SetOutputType
title: IMediaObject::SetOutputType method
author: windows-driver-content
description: The SetOutputType method sets the media type on an output stream, or tests whether a media type is acceptable.
old-location: dshow\imediaobject_setoutputtype.htm
old-project: DirectShow
ms.assetid: 1dda3c55-d37b-4e04-9509-0e5197d6b019
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IMediaObject, IMediaObject interface [DirectShow], SetOutputType method, IMediaObject::SetOutputType, IMediaObjectSetOutputType, SetOutputType method [DirectShow], SetOutputType method [DirectShow], IMediaObject interface, SetOutputType,IMediaObject.SetOutputType, dshow.imediaobject_setoutputtype, mediaobj/IMediaObject::SetOutputType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mediaobj.h
req.include-header: Dmo.h
req.target-type: Windows
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Dmoguids.lib
-	Dmoguids.dll
api_name:
-	IMediaObject.SetOutputType
product: Windows
targetos: Windows
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMediaObject::SetOutputType method


## -description



The <code>SetOutputType</code> method sets the media type on an output stream, or tests whether a media type is acceptable.




## -parameters




### -param dwOutputStreamIndex

Zero-based index of an output stream on the DMO.


### -param pmt [in]

Pointer to a <a href="https://msdn.microsoft.com/c545ddf7-9797-45ab-a42a-d8550b598e98">DMO_MEDIA_TYPE</a> structure that specifies the media type.


### -param dwFlags

Bitwise combination of zero or more flags from the <a href="https://msdn.microsoft.com/e0638668-bbd2-4696-8482-d72438510740">DMO_SET_TYPE_FLAGS</a> enumeration.


## -returns



Returns an <b>HRESULT</b> value. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMO_E_INVALIDSTREAMINDEX</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream index

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMO_E_TYPE_NOT_ACCEPTED</b></dt>
</dl>
</td>
<td width="60%">
Media type was not accepted

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Media type is not acceptable

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Media type was set successfully, or is acceptable

</td>
</tr>
</table>
 




## -remarks



Call this method to test, set, or clear the media type on an output stream:

<ul>
<li>To test the media type without setting it, use the DMO_SET_TYPEF_TEST_ONLY flag. If the media type is not acceptable, the method returns S_FALSE.</li>
<li>To set the media type, set <i>dwFlags</i> to zero. If the media type is not acceptable, the method returns DMO_E_TYPE_NOT_ACCEPTED.</li>
<li>To clear the current media type (if any), use the DMO_SET_TYPEF_CLEAR flag and set <i>pmt</i> to <b>NULL</b>. When the method returns, the stream no longer has a media type. The DMO cannot process samples until the application sets a new media type, unless the stream is optional.</li>
</ul>
The media types that are currently set on other streams can affect whether the media type is acceptable.




## -see-also




<a href="https://msdn.microsoft.com/a3fd17aa-7df2-40f4-8f2c-45bae38e4c0b">IMediaObject Interface</a>
 

 

