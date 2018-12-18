---
UID: NF:relogger.ITraceRelogger.SetOutputFilename
title: ITraceRelogger::SetOutputFilename
author: windows-sdk-content
description: Indicates the file to which ETW should write the new, relogged trace.
old-location: etw\itracerelogger_setoutputfilename.htm
tech.root: etw
ms.assetid: ed3f8bcd-88c7-4d05-a396-41ee8f35bc97
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITraceRelogger interface [ETW],SetOutputFilename method, ITraceRelogger.SetOutputFilename, ITraceRelogger::SetOutputFilename, SetOutputFilename, SetOutputFilename method [ETW], SetOutputFilename method [ETW],ITraceRelogger interface, etw.itracerelogger_setoutputfilename, relogger/ITraceRelogger::SetOutputFilename
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Relogger.h
api_name:
 - ITraceRelogger.SetOutputFilename
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITraceRelogger::SetOutputFilename


## -description


The <b>SetOutputFilename</b> method indicates the file to which ETW should write the new, relogged trace.


## -parameters




### -param LogfileName [in]

Type: <b>BSTR</b>

The new filename.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the indicated file already exists, it will be overwritten with the new trace.




## -see-also




<a href="https://msdn.microsoft.com/08073b9a-5ae0-4e88-a502-647567418005">ITraceRelogger</a>
 

 

