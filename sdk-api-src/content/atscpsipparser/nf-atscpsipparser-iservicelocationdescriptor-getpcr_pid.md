---
UID: NF:atscpsipparser.IServiceLocationDescriptor.GetPCR_PID
title: IServiceLocationDescriptor::GetPCR_PID
author: windows-sdk-content
description: Gets the program ID (PID) for the packets that contain the Program Clock Reference (PCR) in the transport stream from an Advanced Television Systems Committee (ATSC) Service Location Descriptor.
old-location: mstv\iservicelocationdescriptor_getpcr_pid.htm
old-project: mstv
ms.assetid: a81a2218-3c44-4b17-a5cb-bb68d10da977
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetPCR_PID, GetPCR_PID method [Microsoft TV Technologies], GetPCR_PID method [Microsoft TV Technologies],IServiceLocationDescriptor interface, IServiceLocationDescriptor interface [Microsoft TV Technologies],GetPCR_PID method, IServiceLocationDescriptor.GetPCR_PID, IServiceLocationDescriptor::GetPCR_PID, atscpsipparser/IServiceLocationDescriptor::GetPCR_PID, mstv.iservicelocationdescriptor_getpcr_pid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: atscpsipparser.h
req.include-header: Atscpsipparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: AsyncStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	atscpsipparser.h
api_name:
-	IServiceLocationDescriptor.GetPCR_PID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IServiceLocationDescriptor::GetPCR_PID


## -description


Gets the program ID (PID) for the packets that contain the Program Clock Reference (PCR) in the transport stream from an Advanced Television Systems Committee (ATSC) Service Location Descriptor. 


## -parameters




### -param pwVal [out]

Receives the PID value.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/43dd800b-c51d-4a2f-ad59-943cb4975066">IServiceLocationDescriptor</a>
 

 

