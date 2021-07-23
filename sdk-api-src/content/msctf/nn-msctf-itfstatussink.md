---
UID: NN:msctf.ITfStatusSink
title: ITfStatusSink (msctf.h)
description: The ITfStatusSink interface supports changes to the global document status. This advise sink is installed by calling ITfSource::AdviseSink with IID_ITfStatusSink. A text service can optionally implement this interface.
helpviewer_keywords: ["ITfStatusSink","ITfStatusSink interface [Text Services Framework]","ITfStatusSink interface [Text Services Framework]","described","_tsf_itfstatussink_ref","msctf/ITfStatusSink","tsf.itfstatussink"]
old-location: tsf\itfstatussink.htm
tech.root: TSF
ms.assetid: 5fc37251-938b-4581-bb54-816749b17001
ms.date: 12/05/2018
ms.keywords: ITfStatusSink, ITfStatusSink interface [Text Services Framework], ITfStatusSink interface [Text Services Framework],described, _tsf_itfstatussink_ref, msctf/ITfStatusSink, tsf.itfstatussink
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Tiptsf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfStatusSink
 - msctf/ITfStatusSink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tiptsf.dll
api_name:
 - ITfStatusSink
---

# ITfStatusSink interface


## -description

The <b>ITfStatusSink</b> interface supports changes to the global document status. This advise sink is installed by calling <a href="/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink</a> with IID_ITfStatusSink. A text service can optionally implement this interface.

## -inheritance

The <b>ITfStatusSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfStatusSink</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)">TF_STATUS
      </a>
