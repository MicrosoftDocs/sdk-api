---
UID: NF:imapi.IDiscRecorder.GetBasePnPID
title: IDiscRecorder::GetBasePnPID
author: windows-sdk-content
description: Retrieves a base PnP string that can be used to consistently identify a specific class of device by make and model. The string can be used by applications to customize their behavior according to the specific recorder type.
old-location: imapi\idiscrecorder_getbasepnpid.htm
old-project: imapi
ms.assetid: 02ca36dd-bd76-41b8-90ce-6c026152cdbe
ms.author: windowssdkdev
ms.date: 06/15/2018
ms.keywords: GetBasePnPID, GetBasePnPID method [IMAPI], GetBasePnPID method [IMAPI],IDiscRecorder interface, IDiscRecorder interface [IMAPI],GetBasePnPID method, IDiscRecorder.GetBasePnPID, IDiscRecorder::GetBasePnPID, _win32_idiscrecorder_getbasepnpid, base.idiscrecorder_getbasepnpid, imapi.idiscrecorder_getbasepnpid, imapi/IDiscRecorder::GetBasePnPID
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: imapi.h
req.include-header: 
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
 - IDiscRecorder.GetBasePnPID
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
req.product: GDI+ 1.1
---

# IDiscRecorder::GetBasePnPID


## -description


Retrieves a base PnP string that can be used to consistently identify a specific class of device by make and model. The string can be used by applications to customize their behavior according to the specific recorder type.


## -parameters




### -param pbstrBasePnPID [out]

Base PnP ID string. The string is a concatenation of a recorder's manufacturer, product ID, and revision information (if available).


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -see-also




<a href="https://msdn.microsoft.com/fc861cbb-a14e-499e-8b80-f5912e4f6076">IDiscRecorder</a>
 

 

