---
UID: NF:cscobj.IOfflineFilesProgress.End
title: IOfflineFilesProgress::End (cscobj.h)
description: Reports that an operation has ended.
helpviewer_keywords: ["End","End method [Offline Files]","End method [Offline Files]","IOfflineFilesProgress interface","IOfflineFilesProgress interface [Offline Files]","End method","IOfflineFilesProgress.End","IOfflineFilesProgress::End","cscobj/IOfflineFilesProgress::End","of.iofflinefilesprogress_end"]
old-location: of\iofflinefilesprogress_end.htm
tech.root: of
ms.assetid: b3d09f2e-29d5-496f-a046-4ba067e642a6
ms.date: 12/05/2018
ms.keywords: End, End method [Offline Files], End method [Offline Files],IOfflineFilesProgress interface, IOfflineFilesProgress interface [Offline Files],End method, IOfflineFilesProgress.End, IOfflineFilesProgress::End, cscobj/IOfflineFilesProgress::End, of.iofflinefilesprogress_end
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOfflineFilesProgress::End
 - cscobj/IOfflineFilesProgress::End
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesProgress.End
---

# IOfflineFilesProgress::End


## -description

Reports that an operation has ended.

## -parameters

### -param hrResult [in]

Indicates the result of the operation as a whole.  Contains S_OK if the operation completed successfully,  HRESULT_FROM_WIN32(ERROR_CANCELLED) if the operation was canceled or an error value otherwise.

## -returns

The return value is ignored.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesprogress">IOfflineFilesProgress</a>