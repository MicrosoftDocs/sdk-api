---
UID: NF:restrictederrorinfo.ILanguageExceptionStackBackTrace.GetStackBackTrace
title: ILanguageExceptionStackBackTrace::GetStackBackTrace (restrictederrorinfo.h)
description: Retrieves the back stack trace.
helpviewer_keywords: ["GetStackBackTrace","GetStackBackTrace method [Windows Runtime]","GetStackBackTrace method [Windows Runtime]","ILanguageExceptionStackBackTrace interface","ILanguageExceptionStackBackTrace interface [Windows Runtime]","GetStackBackTrace method","ILanguageExceptionStackBackTrace.GetStackBackTrace","ILanguageExceptionStackBackTrace::GetStackBackTrace","restrictederrorinfo/ILanguageExceptionStackBackTrace::GetStackBackTrace","winrt.ilanguageexceptionstackbacktrace_getstackbacktrace"]
old-location: winrt\ilanguageexceptionstackbacktrace_getstackbacktrace.htm
tech.root: WinRT
ms.assetid: 6EB89F76-C518-41A3-A1F8-EC480B0FC68B
ms.date: 12/05/2018
ms.keywords: GetStackBackTrace, GetStackBackTrace method [Windows Runtime], GetStackBackTrace method [Windows Runtime],ILanguageExceptionStackBackTrace interface, ILanguageExceptionStackBackTrace interface [Windows Runtime],GetStackBackTrace method, ILanguageExceptionStackBackTrace.GetStackBackTrace, ILanguageExceptionStackBackTrace::GetStackBackTrace, restrictederrorinfo/ILanguageExceptionStackBackTrace::GetStackBackTrace, winrt.ilanguageexceptionstackbacktrace_getstackbacktrace
req.header: restrictederrorinfo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Restrictederrorinfo.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ILanguageExceptionStackBackTrace::GetStackBackTrace
 - restrictederrorinfo/ILanguageExceptionStackBackTrace::GetStackBackTrace
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - restrictederrorinfo.h
api_name:
 - ILanguageExceptionStackBackTrace.GetStackBackTrace
---

# ILanguageExceptionStackBackTrace::GetStackBackTrace


## -description

Retrieves the back stack trace.

## -parameters

### -param maxFramesToCapture [in]

The maximum number of frames to capture.

### -param stackBackTrace [in, out]

An array containing the stack back trace; the maximum size is the <i>maxFramesToCapture</i>.

### -param framesCaptured [out]

On success, contains a pointer to the number of frames actually captured.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You should implement <b>GetStackBackTrace</b> in your language projections when the Global Error Handler surface is unable to capture a backtrace. <b>GetStackBackTrace</b> is called by the <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rooriginatelanguageexception">RoOriginateLanguageException</a> export and by <a href="/windows/desktop/api/restrictederrorinfo/nf-restrictederrorinfo-ilanguageexceptionerrorinfo2-capturepropagationcontext">CapturePropagationContext</a> when those functions detect, through querying for interface (QI), that the language exception provided to them implements it.

## -see-also

<a href="/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptionstackbacktrace">ILanguageExceptionStackBackTrace</a>