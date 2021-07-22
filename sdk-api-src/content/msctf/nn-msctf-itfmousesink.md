---
UID: NN:msctf.ITfMouseSink
title: ITfMouseSink (msctf.h)
description: The ITfMouseSink interface is implemented by a text service to receive mouse event notifications. A mouse event sink is installed with the ITfMouseTracker::AdviseMouseSink method of one of the ITfMouseTracker interfaces.
helpviewer_keywords: ["ITfMouseSink","ITfMouseSink interface [Text Services Framework]","ITfMouseSink interface [Text Services Framework]","described","_tsf_itfmousesink_ref","msctf/ITfMouseSink","tsf.itfmousesink"]
old-location: tsf\itfmousesink.htm
tech.root: TSF
ms.assetid: d6e5549e-768d-47af-a553-84430641cda4
ms.date: 12/05/2018
ms.keywords: ITfMouseSink, ITfMouseSink interface [Text Services Framework], ITfMouseSink interface [Text Services Framework],described, _tsf_itfmousesink_ref, msctf/ITfMouseSink, tsf.itfmousesink
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
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfMouseSink
 - msctf/ITfMouseSink
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
 - ITfMouseSink
---

# ITfMouseSink interface


## -description

The <b>ITfMouseSink</b> interface is implemented by a text service to receive mouse event notifications. A mouse event sink is installed with the <a href="/windows/desktop/api/msctf/nf-msctf-itfmousetracker-advisemousesink">ITfMouseTracker::AdviseMouseSink</a> method of one of the <a href="/windows/desktop/api/msctf/nn-msctf-itfmousetracker">ITfMouseTracker</a> interfaces.

## -inheritance

The <b>ITfMouseSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfMouseSink</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfmousetracker-advisemousesink">ITfMouseTracker::AdviseMouseSink
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfmousetrackeracp-advisemousesink">ITfMouseTrackerACP::AdviseMouseSink
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
