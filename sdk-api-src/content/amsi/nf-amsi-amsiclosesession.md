---
UID: NF:amsi.AmsiCloseSession
title: AmsiCloseSession function (amsi.h)
description: Close a session that was opened by AmsiOpenSession.
helpviewer_keywords: ["AmsiCloseSession","AmsiCloseSession function [Antimalware Scan Interface]","amsi.amsiclosesession","amsi/AmsiCloseSession"]
old-location: amsi\amsiclosesession.htm
tech.root: AMSI
ms.assetid: 1DF760A2-22AE-427E-8395-1EE34BD7BCAB
ms.date: 12/05/2018
ms.keywords: AmsiCloseSession, AmsiCloseSession function [Antimalware Scan Interface], amsi.amsiclosesession, amsi/AmsiCloseSession
req.header: amsi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Amsi.lib
req.dll: Amsi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AmsiCloseSession
 - amsi/AmsiCloseSession
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - amsi.dll
api_name:
 - AmsiCloseSession
---

# AmsiCloseSession function


## -description

Close a session that was opened by <a href="/windows/desktop/api/amsi/nf-amsi-amsiopensession">AmsiOpenSession</a>.

## -parameters

### -param amsiContext [in]

The handle of type HAMSICONTEXT that was initially received from <a href="/windows/desktop/api/amsi/nf-amsi-amsiinitialize">AmsiInitialize</a>.

### -param amsiSession [in]

The handle of type HAMSISESSION that was initially received from <a href="/windows/desktop/api/amsi/nf-amsi-amsiopensession">AmsiOpenSession</a>.

## -see-also

<a href="/windows/desktop/api/amsi/nf-amsi-amsiinitialize">AmsiInitialize</a>



<a href="/windows/desktop/api/amsi/nf-amsi-amsiopensession">AmsiOpenSession</a>