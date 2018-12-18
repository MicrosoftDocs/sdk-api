---
UID: NF:atscpsipparser.IServiceLocationDescriptor.GetElementPID
title: IServiceLocationDescriptor::GetElementPID
author: windows-sdk-content
description: Gets the program ID (PID) that identifies an elementary stream from an Advanced Television Systems Committee (ATSC) Service Location Descriptor.
old-location: mstv\iservicelocationdescriptor_getelementpid.htm
tech.root: mstv
ms.assetid: 97b6091b-cacb-4e69-8ca4-c9f4b70f6304
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetElementPID, GetElementPID method [Microsoft TV Technologies], GetElementPID method [Microsoft TV Technologies],IServiceLocationDescriptor interface, IServiceLocationDescriptor interface [Microsoft TV Technologies],GetElementPID method, IServiceLocationDescriptor.GetElementPID, IServiceLocationDescriptor::GetElementPID, atscpsipparser/IServiceLocationDescriptor::GetElementPID, mstv.iservicelocationdescriptor_getelementpid
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - IServiceLocationDescriptor.GetElementPID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IServiceLocationDescriptor::GetElementPID


## -description


Gets the program ID (PID) that identifies an elementary stream from an Advanced Television Systems Committee (ATSC) Service Location Descriptor. 


## -parameters




### -param bIndex [in]

Specifies the elementary stream,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/134e4051-6a73-4420-b12d-3171738bd8ad">IServiceLocationDescriptor::GetNumberOfElements</a>method to get the number of elementary streams in the descriptor.


### -param pwVal [out]

Receives the PID value for the elementary stream.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/43dd800b-c51d-4a2f-ad59-943cb4975066">IServiceLocationDescriptor</a>
 

 

