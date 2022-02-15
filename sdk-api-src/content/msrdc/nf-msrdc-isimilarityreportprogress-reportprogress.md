---
UID: NF:msrdc.ISimilarityReportProgress.ReportProgress
title: ISimilarityReportProgress::ReportProgress (msrdc.h)
description: Reports the current completion percentage of a similarity operation in progress.
helpviewer_keywords: ["ISimilarityReportProgress interface [Remote Differential Compression]","ReportProgress method","ISimilarityReportProgress.ReportProgress","ISimilarityReportProgress::ReportProgress","ReportProgress","ReportProgress method [Remote Differential Compression]","ReportProgress method [Remote Differential Compression]","ISimilarityReportProgress interface","fs.isimilarityreportprogress_reportprogress","msrdc/ISimilarityReportProgress::ReportProgress","rdc.isimilarityreportprogress_reportprogress"]
old-location: rdc\isimilarityreportprogress_reportprogress.htm
tech.root: rdc
ms.assetid: e393290b-02d3-4265-9252-f5541e4054ce
ms.date: 12/05/2018
ms.keywords: ISimilarityReportProgress interface [Remote Differential Compression],ReportProgress method, ISimilarityReportProgress.ReportProgress, ISimilarityReportProgress::ReportProgress, ReportProgress, ReportProgress method [Remote Differential Compression], ReportProgress method [Remote Differential Compression],ISimilarityReportProgress interface, fs.isimilarityreportprogress_reportprogress, msrdc/ISimilarityReportProgress::ReportProgress, rdc.isimilarityreportprogress_reportprogress
req.header: msrdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsRdc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: MsRdc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISimilarityReportProgress::ReportProgress
 - msrdc/ISimilarityReportProgress::ReportProgress
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - ISimilarityReportProgress.ReportProgress
---

# ISimilarityReportProgress::ReportProgress


## -description

Reports the current completion percentage of a similarity operation in progress.

## -parameters

### -param percentCompleted [in]

The current completion percentage of the task. The valid range is from 0 through 100.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilarity-copyandswap">ISimilarity::CopyAndSwap</a> method calls the <b>ReportProgress</b>  method to report the progress of the copy-and-swap operation. To receive the progress information, RDC applications must implement this method.

No guarantee is made as to how frequently this method is called, nor that it will be called with any specific values for the <i>percentCompleted</i> parameter. For example, the <i>percentCompleted</i> parameter may not start at zero and may never reach 100, and it may receive the same value more than once. However, each value is guaranteed to be greater than or equal to the previous value.

If the application returns an error code such as <b>E_FAIL</b>, the similarity operation is stopped, and the error code is propagated.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilarityreportprogress">ISimilarityReportProgress</a>