---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IMFHttpDownloadRequest::GetTimeSeekResult


## -description


Invoked by Microsoft Media Foundation to retrieve the values of the TimeSeekRange.DLNA.ORG HTTP header, if any, that the server specified in its response.


## -parameters




### -param pqwStartTime [out]

The starting time offset, specified in units of one-hundred nanoseconds.

The time duration of data contained in the response, specified in units of one-hundred nanoseconds. Set this parameter to 0 if the server did not specify a duration (i.e., specified “*” as the duration.)


### -param pqwStopTime [out]

The end time offset, specified in units of one-hundred nanoseconds


### -param pqwDuration






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
The TimeSeekRange.DLNA.ORG HTTP header was present in the response, and could be successfully parsed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The TimeSeekRange.DLNA.ORG HTTP header was not present in the response, or had a syntax error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">

                The <i>pfNullSOurceOrigin</i> parameter is an invalid pointer.

</td>
</tr>
</table>
 




## -remarks



The values of all the parameters should be set to 0 if <b>GetTimeSeekResult</b> is invoked before <a href="https://msdn.microsoft.com/FC342FB9-930F-4EA7-9057-51AF10D13ED9">EndReceiveResponse</a> has been invoked. For information about the syntax for the TimeSeekRange.DLNA.ORG header, please refer to the <a href="http://www.dlna.org/guidelines/">DLNA web site</a>.




## -see-also




<a href="https://msdn.microsoft.com/A8A37C2F-A662-4FDA-95F6-43D96A8471A8">IMFHttpDownloadRequest</a>
 

 

