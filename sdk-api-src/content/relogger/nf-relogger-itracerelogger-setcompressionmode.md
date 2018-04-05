---
UID: NF:relogger.ITraceRelogger.SetCompressionMode
title: ITraceRelogger::SetCompressionMode method
author: windows-driver-content
description: Enables or disables compression on the relogged trace.
old-location: etw\itracerelogger_setcompressionmode.htm
old-project: ETW
ms.assetid: 2a758af0-2316-4c4b-8717-ee1ebad205ee
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITraceRelogger, ITraceRelogger interface [ETW], SetCompressionMode method, ITraceRelogger::SetCompressionMode, SetCompressionMode method [ETW], SetCompressionMode method [ETW], ITraceRelogger interface, SetCompressionMode,ITraceRelogger.SetCompressionMode, etw.itracerelogger_setcompressionmode, relogger/ITraceRelogger::SetCompressionMode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: relogger.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Relogger.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RECO_RANGE, RECO_RANGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Relogger.h
api_name:
-	ITraceRelogger.SetCompressionMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# ITraceRelogger::SetCompressionMode method


## -description


The <b>SetCompressionMode</b> method enables or disables compression on the relogged trace.


## -parameters




### -param CompressionMode [in]

Type: <b>BOOLEAN</b>

True if compression is enabled; otherwise, false.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



By default, compression will be enabled on a relogged trace.

Compression mode is not supported on Windows 7. By default,  Compression mode it is set to <b>false</b> on Windows 7. When this method is called,   it returns <b>E_NOTIMPL</b> when called on Windows 7.


Compression mode is set  to <b>true</b> on Windows 8 or Windows Server 2012.

Compressed trace files can only be decoded in Windows 8 or Windows Server 2012.




## -see-also




<a href="https://msdn.microsoft.com/08073b9a-5ae0-4e88-a502-647567418005">ITraceRelogger</a>
 

 

