---
UID: NF:sbtsv.ITsSbBaseNotifySink.OnReportStatus
title: ITsSbBaseNotifySink::OnReportStatus
author: windows-sdk-content
description: Sends status messages to the Remote Desktop Connection (RDC) client regarding the processing of a client connection.
old-location: termserv\itssbbasenotifysink_onreportstatus.htm
tech.root: TermServ
ms.assetid: 4bde8375-b03a-44b8-9ba5-bc15277f3a4a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CLIENT_MESSAGE_CONNECTION_ERROR, CLIENT_MESSAGE_CONNECTION_STATUS, ITsSbBaseNotifySink interface [Remote Desktop Services],OnReportStatus method, ITsSbBaseNotifySink.OnReportStatus, ITsSbBaseNotifySink::OnReportStatus, OnReportStatus, OnReportStatus method [Remote Desktop Services], OnReportStatus method [Remote Desktop Services],ITsSbBaseNotifySink interface, TS_STATUS_VM_BOOTING, TS_STATUS_VM_LOADING, TS_STATUS_VM_WAKING, sbtsv/ITsSbBaseNotifySink::OnReportStatus, termserv.itssbbasenotifysink_onreportstatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbBaseNotifySink.OnReportStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

