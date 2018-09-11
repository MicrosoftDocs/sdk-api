---
UID: NS:wmsdkidl._WMStreamPrioritizationRecord
title: "_WMStreamPrioritizationRecord"
author: windows-sdk-content
description: The WM_STREAM_PRIORITY_RECORD structure contains a stream number and specifies whether delivery of that stream is mandatory.
old-location: wmformat\wm_stream_priority_record.htm
tech.root: wmformat
ms.assetid: 43c9370c-cd43-4dd0-8258-d6dbdb98f1de
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WM_STREAM_PRIORITY_RECORD, WM_STREAM_PRIORITY_RECORD structure [windows Media Format], _WMStreamPrioritizationRecord, wmformat.wm_stream_priority_record, wmsdkidl/WM_STREAM_PRIORITY_RECORD
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - WM_STREAM_PRIORITY_RECORD
product: Windows
targetos: Windows
req.typenames: WM_STREAM_PRIORITY_RECORD
req.redist: 
---

# _WMStreamPrioritizationRecord structure


## -description



The <b>WM_STREAM_PRIORITY_RECORD</b> structure contains a stream number and specifies whether delivery of that stream is mandatory.




## -struct-fields




### -field wStreamNumber

<b>WORD</b> containing the stream number.


### -field fMandatory

Flag indicating whether the listed stream is mandatory. Mandatory streams will not be dropped regardless of their position in the priority list.


## -remarks



<b>WM_STREAM_PRIORITY_RECORD</b> is used in an array by the <b>IWMStreamPrioritization</b> interface. Each member of the array specifies a stream; the lower the element number in the array, the higher the priority of the stream.




## -see-also




<a href="https://msdn.microsoft.com/ef8ae275-c36a-492c-b57c-d640044ede93">IWMStreamPrioritization Interface</a>



<a href="https://msdn.microsoft.com/118ef278-ca4f-4c30-9633-a2d851f5c758">Structures</a>
 

 

