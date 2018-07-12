---
UID: NF:wmcontainer.IMFASFMultiplexer.End
title: IMFASFMultiplexer::End
author: windows-sdk-content
description: Collects data from the multiplexer and updates the ASF ContentInfo object to include that information in the ASF Header Object.
old-location: mf\imfasfmultiplexer_end.htm
old-project: medfound
ms.assetid: 2a106ea5-976a-40df-a554-1b76d9a07286
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: 2a106ea5-976a-40df-a554-1b76d9a07286, End, End method [Media Foundation], End method [Media Foundation],IMFASFMultiplexer interface, IMFASFMultiplexer interface [Media Foundation],End method, IMFASFMultiplexer.End, IMFASFMultiplexer::End, mf.imfasfmultiplexer_end, wmcontainer/IMFASFMultiplexer::End
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MFASF_STREAMSELECTOR_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFMultiplexer.End
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

