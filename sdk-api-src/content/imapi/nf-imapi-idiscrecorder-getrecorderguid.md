---
UID: NF:imapi.IDiscRecorder.GetRecorderGUID
title: IDiscRecorder::GetRecorderGUID
author: windows-sdk-content
description: Retrieves the GUID of the physical disc recorder currently associated with the recorder object.
old-location: imapi\idiscrecorder_getrecorderguid.htm
old-project: imapi
ms.assetid: 9d13d352-bc48-43c7-9800-12855d754435
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetRecorderGUID, GetRecorderGUID method [IMAPI], GetRecorderGUID method [IMAPI],IDiscRecorder interface, IDiscRecorder interface [IMAPI],GetRecorderGUID method, IDiscRecorder.GetRecorderGUID, IDiscRecorder::GetRecorderGUID, _win32_idiscrecorder_getrecorderguid, base.idiscrecorder_getrecorderguid, imapi.idiscrecorder_getrecorderguid, imapi/IDiscRecorder::GetRecorderGUID
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: imapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: AM_LINE21_DRAWBGMODE, *PAM_LINE21_DRAWBGMODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Actxprxy.dll
api_name:
 - IDiscRecorder.GetRecorderGUID
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
req.product: GDI+ 1.1
---

# IDiscRecorder::GetRecorderGUID


## -description


Retrieves the GUID of the physical disc recorder currently associated with the recorder object.


## -parameters




### -param pbyUniqueID [in]

Pointer to a GUID buffer to be filled in with this recorder's current GUID information. To query the required buffer size, use <b>NULL</b>.


### -param ulBufferSize [in]

Size of the GUID buffer. If <i>pbyUniqueID</i> is <b>NULL</b>, this parameter must be zero.


### -param pulReturnSizeRequired [out]

Size of the GUID information.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -see-also




<a href="https://msdn.microsoft.com/fc861cbb-a14e-499e-8b80-f5912e4f6076">IDiscRecorder</a>
 

 

