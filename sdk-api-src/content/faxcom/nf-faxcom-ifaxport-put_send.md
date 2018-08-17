---
UID: NF:faxcom.IFaxPort.put_Send
title: IFaxPort::put_Send
author: windows-sdk-content
description: The Send property is a Boolean value that indicates whether a fax port is enabled to send faxes.
old-location: fax\_mfax_ifaxport_get_send_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_9uqs.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: FaxPort object [Fax Service],Send property, FaxPort.Send, IFaxPort.put_Send, IFaxPort::put_Send, Send property [Fax Service], Send property [Fax Service],FaxPort object, _mfax_ifaxport_get_send, fax._mfax_ifaxport_get_send, fax._mfax_ifaxport_get_send_vb, put_Send
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: faxcom.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: ShellWindowTypeConstants
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - FaxPort.Send
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxPort::put_Send


## -description


The <b>Send</b> property is a Boolean value that indicates whether a fax port is enabled to send faxes. 

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  Before setting a value for this property, a fax client application can call the <a href="https://msdn.microsoft.com/c88c2855-51cd-404e-a89f-cc42f456f51c">CanModify</a> property to ensure that the client has permission to modify configuration information for the specified fax port.</div>
<div> </div>
The <b>Send</b> property returns a value of TRUE if the fax port is enabled to send faxes. If a fax client application passes a value of TRUE to the property, it enables the fax port to send faxes. 




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/7888d042-7d85-4921-b233-f6e95e0c80d9">FaxPort</a>



<a href="https://msdn.microsoft.com/abdd91dd-7734-411a-9b7c-0da312269e6d">IFaxPort</a>



<a href="https://msdn.microsoft.com/e61b13b3-d86c-4f95-bf5a-6b0545a76d03">IFaxPorts</a>
 

 

