---
UID: NF:mfidl.IMFWorkQueueServices.GetPlaftormWorkQueueMMCSSClass
title: IMFWorkQueueServices::GetPlaftormWorkQueueMMCSSClass
author: windows-sdk-content
description: Retrieves the Multimedia Class Scheduler Service (MMCSS) class for a specified platform work queue.
old-location: mf\imfworkqueueservices_getplaftormworkqueuemmcssclass.htm
tech.root: medfound
ms.assetid: f953a54b-2bc0-4ddc-9837-57f72e564c02
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetPlaftormWorkQueueMMCSSClass, GetPlaftormWorkQueueMMCSSClass method [Media Foundation], GetPlaftormWorkQueueMMCSSClass method [Media Foundation],IMFWorkQueueServices interface, IMFWorkQueueServices interface [Media Foundation],GetPlaftormWorkQueueMMCSSClass method, IMFWorkQueueServices.GetPlaftormWorkQueueMMCSSClass, IMFWorkQueueServices::GetPlaftormWorkQueueMMCSSClass, f953a54b-2bc0-4ddc-9837-57f72e564c02, mf.imfworkqueueservices_getplaftormworkqueuemmcssclass, mfidl/IMFWorkQueueServices::GetPlaftormWorkQueueMMCSSClass
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
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
 - IMFWorkQueueServices.GetPlaftormWorkQueueMMCSSClass
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mfidl.h
: 
- IMFWorkQueueServices.GetPlaftormWorkQueueMMCSSClass
: 
---

# IMFWorkQueueServices::GetPlaftormWorkQueueMMCSSClass


## -description



Retrieves the Multimedia Class Scheduler Service (MMCSS) class for a specified platform work queue.




## -parameters




### -param dwPlatformWorkQueueId [in]

Platform work queue to query. See <a href="https://msdn.microsoft.com/aea9f946-dd59-4e51-a1de-b086e70ea083">IMFWorkQueueServices::BeginRegisterPlatformWorkQueueWithMMCSS</a>.


### -param pwszClass [out]

Pointer to a buffer that receives the name of the MMCSS class. This parameter can be <b>NULL</b>.


### -param pcchClass [in, out]

On input, specifies the size of the pwszClass buffer, in characters. On output, receives the required size of the buffer, in characters. The size includes the terminating null character.


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
<dt><b>MF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The <i>pwszClass</i> buffer is too small to receive the class name.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7a6ddb67-9a8c-408c-b750-4f3fd3ba0d7d">IMFWorkQueueServices</a>
 

 

