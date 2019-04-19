---
UID: NF:imapi2.IDiscFormat2TrackAtOnce.put_Recorder
title: IDiscFormat2TrackAtOnce::put_Recorder (imapi2.h)
author: windows-sdk-content
description: Sets the recording device to use for the write operation.
old-location: imapi\idiscformat2trackatonce_put_recorder.htm
tech.root: imapi
ms.assetid: 6d67b076-0c3f-4d1f-aa19-8e22dd98f331
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDiscFormat2TrackAtOnce interface [IMAPI],put_Recorder method, IDiscFormat2TrackAtOnce.put_Recorder, IDiscFormat2TrackAtOnce::put_Recorder, imapi.idiscformat2trackatonce_put_recorder, imapi2/IDiscFormat2TrackAtOnce::put_Recorder, put_Recorder, put_Recorder method [IMAPI], put_Recorder method [IMAPI],IDiscFormat2TrackAtOnce interface
ms.topic: method
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - imapi2.h
api_name:
 - IDiscFormat2TrackAtOnce.put_Recorder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDiscFormat2TrackAtOnce::put_Recorder


## -description


Sets the recording device to use for the write operation.


## -parameters




### -param value [in]

An <a href="https://msdn.microsoft.com/34f858b8-74eb-4725-8815-7954cb98cff0">IDiscRecorder2</a> interface that identifies the recording device to use in the write operation.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2TAO_WRITE_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
A write operation is in progress.

Value: 0xC0AA0500

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2TAO_MEDIA_IS_PREPARED</b></dt>
</dl>
</td>
<td width="60%">
The requested operation is not valid when media has been "prepared" but not released.

Value: 0xC0AA0503

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
This device does not support the operations required by this disc format.

Value: 0xC0AA050E

</td>
</tr>
</table>
 




## -remarks



The recorder must be compatible with the format defined by this  interface. To determine compatibility, call the <a href="https://msdn.microsoft.com/1a96283a-a5a3-434a-834a-d539160cfc5c">IDiscFormat2::IsRecorderSupported</a> method.




## -see-also




<a href="https://msdn.microsoft.com/27f2d248-1c83-4784-82f9-75ce0a038b87">IDiscFormat2TrackAtOnce</a>



<a href="https://msdn.microsoft.com/62a60ffb-4a9b-4921-b7fa-acc5a439e92b">IDiscFormat2TrackAtOnce::get_Recorder</a>
 

 

