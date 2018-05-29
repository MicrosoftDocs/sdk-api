---
UID: NF:sbe.ISBE2MediaTypeProfile.DeleteStream
title: ISBE2MediaTypeProfile::DeleteStream
author: windows-sdk-content
description: Removes a stream from a media type profile.
old-location: mstv\isbe2mediatypeprofile_deletestream.htm
old-project: mstv
ms.assetid: 83e8b802-d28f-4130-addf-772682ac327f
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: DeleteStream, DeleteStream method [Microsoft TV Technologies], DeleteStream method [Microsoft TV Technologies],ISBE2MediaTypeProfile interface, ISBE2MediaTypeProfile interface [Microsoft TV Technologies],DeleteStream method, ISBE2MediaTypeProfile.DeleteStream, ISBE2MediaTypeProfile::DeleteStream, mstv.isbe2mediatypeprofile_deletestream, sbe/ISBE2MediaTypeProfile::DeleteStream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbe.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: STREAMBUFFER_ATTR_DATATYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	sbe.dll
api_name:
-	ISBE2MediaTypeProfile.DeleteStream
product: Windows
targetos: Windows
req.lib: 
req.dll: Sbe.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISBE2MediaTypeProfile::DeleteStream


## -description


Removes a stream from a media type  profile.


## -parameters




### -param Index [in]

The index of the stream to remove. To get the number of the streams in the profile, call the <a href="https://msdn.microsoft.com/9f129ed8-3b61-4291-8400-a5f0905c8b49">ISBE2MediaTypeProfile::GetStreamCount</a> method.


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
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_INVALIDARG</b></b></dt>
</dl>
</td>
<td width="60%">
Invalid parameter.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b2fb3d08-cbef-4dbf-a60b-8363ccee4fbf">ISBE2MediaTypeProfile</a>
 

 

