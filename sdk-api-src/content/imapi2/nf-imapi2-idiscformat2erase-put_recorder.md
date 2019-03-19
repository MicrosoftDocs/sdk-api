---
UID: NF:imapi2.IDiscFormat2Erase.put_Recorder
title: IDiscFormat2Erase::put_Recorder (imapi2.h)
author: windows-sdk-content
description: Sets the recording device to use in the erase operation.
old-location: imapi\idiscformat2erase_put_recorder.htm
tech.root: imapi
ms.assetid: d38c0d75-eb9c-4b8c-bf0e-7f05eb2f5116
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDiscFormat2Erase interface [IMAPI],put_Recorder method, IDiscFormat2Erase.put_Recorder, IDiscFormat2Erase::put_Recorder, imapi.idiscformat2erase_put_recorder, imapi2/IDiscFormat2Erase::put_Recorder, put_Recorder, put_Recorder method [IMAPI], put_Recorder method [IMAPI],IDiscFormat2Erase interface
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
 - IDiscFormat2Erase.put_Recorder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscFormat2Erase::put_Recorder


## -description


Sets the recording device to use in the erase operation.


## -parameters




### -param value [in]

An <a href="https://msdn.microsoft.com/34f858b8-74eb-4725-8815-7954cb98cff0">IDiscRecorder2</a> interface that identifies the recording device to use in the erase operation.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -remarks



The recorder must be compatible with the format defined by this  interface. To determine compatibility, call the <a href="https://msdn.microsoft.com/1a96283a-a5a3-434a-834a-d539160cfc5c">IDiscFormat2::IsRecorderSupported</a> method.




## -see-also




<a href="https://msdn.microsoft.com/3789c876-f42c-4f69-b683-96c157d6418d">IDiscFormat2Erase</a>



<a href="https://msdn.microsoft.com/5f41ea99-e467-45ef-8f78-8b0637adf5be">IDiscFormat2Erase::get_Recorder</a>
 

 

