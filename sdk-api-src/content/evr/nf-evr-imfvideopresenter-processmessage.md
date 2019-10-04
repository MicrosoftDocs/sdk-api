---
UID: NF:evr.IMFVideoPresenter.ProcessMessage
title: IMFVideoPresenter::ProcessMessage (evr.h)
author: windows-sdk-content
description: Sends a message to the video presenter. Messages are used to signal the presenter that it must perform some action, or that some event has occurred.
old-location: mf\imfvideopresenter_processmessage.htm
tech.root: medfound
ms.assetid: f7113cb3-2ea9-4d4f-b6c7-ef4e1025cc6d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFVideoPresenter interface [Media Foundation],ProcessMessage method, IMFVideoPresenter.ProcessMessage, IMFVideoPresenter::ProcessMessage, ProcessMessage, ProcessMessage method [Media Foundation], ProcessMessage method [Media Foundation],IMFVideoPresenter interface, evr/IMFVideoPresenter::ProcessMessage, f7113cb3-2ea9-4d4f-b6c7-ef4e1025cc6d, mf.imfvideopresenter_processmessage
ms.topic: method
f1_keywords: 
 - "evr/IMFVideoPresenter.ProcessMessage"
dev_langs:
 - c++
req.header: evr.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoPresenter.ProcessMessage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoPresenter::ProcessMessage


## -description



Sends a message to the video presenter. Messages are used to signal the presenter that it must perform some action, or that some event has occurred.




## -parameters




### -param eMessage [in]

Specifies the message as a member of the <a href="https://docs.microsoft.com/windows/desktop/api/evr/ne-evr-mfvp_message_type">MFVP_MESSAGE_TYPE</a> enumeration.


### -param ulParam [in]

Message parameter. The meaning of this parameter depends on the message type.


## -returns



The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.

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
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The video renderer has been shut down.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/how-to-write-an-evr-presenter">How to Write an EVR Presenter</a>



<a href="https://docs.microsoft.com/windows/desktop/api/evr/nn-evr-imfvideopresenter">IMFVideoPresenter</a>
 

 

