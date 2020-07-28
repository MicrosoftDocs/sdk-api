---
UID: NF:mftransform.IMFTransform.ProcessMessage
title: IMFTransform::ProcessMessage (mftransform.h)
description: Sends a message to the Media Foundation transform (MFT).
helpviewer_keywords: ["IMFTransform interface [Media Foundation]","ProcessMessage method","IMFTransform.ProcessMessage","IMFTransform::ProcessMessage","ProcessMessage","ProcessMessage method [Media Foundation]","ProcessMessage method [Media Foundation]","IMFTransform interface","a6dc67e5-8473-444a-8463-24f411e59565","mf.imftransform_processmessage","mftransform/IMFTransform::ProcessMessage"]
old-location: mf\imftransform_processmessage.htm
tech.root: mf
ms.assetid: a6dc67e5-8473-444a-8463-24f411e59565
ms.date: 12/05/2018
ms.keywords: IMFTransform interface [Media Foundation],ProcessMessage method, IMFTransform.ProcessMessage, IMFTransform::ProcessMessage, ProcessMessage, ProcessMessage method [Media Foundation], ProcessMessage method [Media Foundation],IMFTransform interface, a6dc67e5-8473-444a-8463-24f411e59565, mf.imftransform_processmessage, mftransform/IMFTransform::ProcessMessage
f1_keywords:
- mftransform/IMFTransform.ProcessMessage
dev_langs:
- c++
req.header: mftransform.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfuuid.lib
- mfuuid.dll
api_name:
- IMFTransform.ProcessMessage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTransform::ProcessMessage


## -description


Sends a message to the Media Foundation transform (MFT).
        


## -parameters




### -param eMessage [in]

The message to send, specified as a member of the <a href="https://docs.microsoft.com/windows/desktop/api/mftransform/ne-mftransform-mft_message_type">MFT_MESSAGE_TYPE</a> enumeration.
          


### -param ulParam [in]

Message parameter. The meaning of this parameter depends on the message type.
          


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
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream number. Applies to the <b>MFT_MESSAGE_NOTIFY_END_OF_STREAM</b> message.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_TRANSFORM_TYPE_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
The media type is not set on one or more streams.
              

</td>
</tr>
</table>
 




## -remarks



Before calling this method, set the media types on all input and output streams.
      

The MFT might ignore certain message types. If so, the method returns <b>S_OK</b>. An error code indicates that the transform handles this message type but was unable to process the message in this instance.
      

If <b>MFT_UNIQUE_METHOD_NAMES</b> is defined before including mftransform.h, this method is renamed <b>MFTProcessMessage</b>. See <a href="https://docs.microsoft.com/windows/desktop/medfound/comparison-of-mfts-and-dmos">Creating Hybrid DMO/MFT Objects</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>
 

 

