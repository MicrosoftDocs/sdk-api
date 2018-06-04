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

# ITsSbBaseNotifySink::OnReportStatus


## -description


Sends status messages to the Remote Desktop Connection (RDC) client regarding the processing of a client 
    connection.


## -parameters




### -param messageType [in]

The message type. This parameter must be one of the following values.



#### CLIENT_MESSAGE_CONNECTION_STATUS

A status message.



#### CLIENT_MESSAGE_CONNECTION_ERROR

An error message.


### -param messageID [in]

The message ID. This parameter must be one of the following values.



#### TS_STATUS_VM_LOADING

The virtual machine is loading.



#### TS_STATUS_VM_WAKING

The virtual machine is waking.



#### TS_STATUS_VM_BOOTING

The virtual machine is starting.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method allows plug-ins to send more specific status and error messages to the RDC client, overriding the 
    default status and error messages that Remote Desktop Connection Broker (RD Connection Broker) sends to the client.

The following error codes are defined by RD Connection Broker for use by plug-ins.






## -see-also




<a href="https://msdn.microsoft.com/11ef1bd4-301f-456b-a68b-2f32b75ac5ae">ITsSbBaseNotifySink</a>
 

 

