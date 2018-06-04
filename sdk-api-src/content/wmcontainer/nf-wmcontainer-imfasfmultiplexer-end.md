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

# IMFASFMultiplexer::End


## -description



Collects data from the multiplexer and updates the ASF ContentInfo object to include that information in the ASF Header Object.




## -parameters




### -param pIContentInfo [in]

Pointer to the  <a href="https://msdn.microsoft.com/9f490e6a-f378-45c1-a69d-985c6e884358">IMFASFContentInfo</a> interface of the ContentInfo object. This must be the same object that was used to initialize the multiplexer. The ContentInfo object represents the ASF Header Object of the file for which the multiplexer generated data packets.


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
<dt><b>MF_E_FLUSH_NEEDED</b></dt>
</dl>
</td>
<td width="60%">
There are pending output media samples waiting in the multiplexer. Call <a href="https://msdn.microsoft.com/44a66374-ad9d-4c76-8c95-21a15e071c6d">IMFASFMultiplexer::Flush</a> to force the media samples to be packetized.

</td>
</tr>
</table>
 




## -remarks



For non-live encoding scenarios (such as encoding to a file), the user should call <b>End</b> to update the specified ContentInfo object, adding data that the multiplexer has collected during the packet generation process. The user should then call <a href="https://msdn.microsoft.com/972f5ae7-ad00-4c3b-8ec4-2cef4ce03c4e">IMFASFContentInfo::GenerateHeader</a> and write the output header at the beginning of the ASF file (overwriting the header obtained at the beginning of the encoding session). For more information, see <a href="https://msdn.microsoft.com/f2a76471-3d93-427b-a316-d0967cd20e77">Writing an ASF Header Object for a New File</a>.

During live encoding, it is usually not possible to rewrite the header, so this call is not required for live encoding. (The header in those cases will simply lack some of the information that was not available until the end of the encoding session.)




## -see-also




<a href="https://msdn.microsoft.com/7afa9694-c965-40e2-8549-e32ff48def2a">Generating New ASF Data Packets</a>



<a href="https://msdn.microsoft.com/9f490e6a-f378-45c1-a69d-985c6e884358">IMFASFContentInfo</a>



<a href="https://msdn.microsoft.com/bdb549b5-425b-4f77-b413-723ceb7acd11">IMFASFMultiplexer</a>
 

 

