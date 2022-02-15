---
UID: NN:msctf.ITfDisplayAttributeNotifySink
title: ITfDisplayAttributeNotifySink (msctf.h)
description: The ITfDisplayAttributeNotifySink interface is implemented by an application to receive a notification when display attribute information is updated.
helpviewer_keywords: ["ITfDisplayAttributeNotifySink","ITfDisplayAttributeNotifySink interface [Text Services Framework]","ITfDisplayAttributeNotifySink interface [Text Services Framework]","described","_tsf_itfdisplayattributenotifysink_ref","msctf/ITfDisplayAttributeNotifySink","tsf.itfdisplayattributenotifysink"]
old-location: tsf\itfdisplayattributenotifysink.htm
tech.root: TSF
ms.assetid: c21ff404-af42-488a-90f0-d3f02277c557
ms.date: 12/05/2018
ms.keywords: ITfDisplayAttributeNotifySink, ITfDisplayAttributeNotifySink interface [Text Services Framework], ITfDisplayAttributeNotifySink interface [Text Services Framework],described, _tsf_itfdisplayattributenotifysink_ref, msctf/ITfDisplayAttributeNotifySink, tsf.itfdisplayattributenotifysink
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfDisplayAttributeNotifySink
 - msctf/ITfDisplayAttributeNotifySink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfDisplayAttributeNotifySink
---

# ITfDisplayAttributeNotifySink interface


## -description

The <b>ITfDisplayAttributeNotifySink</b> interface is implemented by an application to receive a notification when display attribute information is updated. This advise sink is installed by calling the TSF manager's <a href="/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink</a> with IID_ITfDisplayAttributeNotifySink.

## -inheritance

The <b>ITfDisplayAttributeNotifySink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfDisplayAttributeNotifySink</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
