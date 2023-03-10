---
UID: NN:msctf.ITfMessagePump
title: ITfMessagePump (msctf.h)
description: The ITfMessagePump interface is implemented by the TSF manager and is used by an application to obtain messages from the application message queue.
helpviewer_keywords: ["ITfMessagePump","ITfMessagePump interface [Text Services Framework]","ITfMessagePump interface [Text Services Framework]","described","_tsf_itfmessagepump_ref","msctf/ITfMessagePump","tsf.itfmessagepump"]
old-location: tsf\itfmessagepump.htm
tech.root: TSF
ms.assetid: f7c3d039-cffc-4ce0-8579-041ba849de6d
ms.date: 12/05/2018
ms.keywords: ITfMessagePump, ITfMessagePump interface [Text Services Framework], ITfMessagePump interface [Text Services Framework],described, _tsf_itfmessagepump_ref, msctf/ITfMessagePump, tsf.itfmessagepump
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
 - ITfMessagePump
 - msctf/ITfMessagePump
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
 - ITfMessagePump
---

# ITfMessagePump interface


## -description

The <b>ITfMessagePump</b> interface is implemented by the TSF manager and is used by an application to obtain messages from the application message queue. The methods of this interface are wrappers for the <a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingarchive-getmessage-vb">GetMessage</a> and <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a> functions. This interface enables the TSF manager to perform any necessary pre-message or post-message processing.

## -inheritance

The <b>ITfMessagePump</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfMessagePump</b> also has these types of members:

## -remarks

If the application is Unicode, it should use the PeekMessageW and GetMessageW methods. Otherwise, the application should use the PeekMessageA and GetMessageA methods.


#### Examples


<a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgr">ITfThreadMgr
          </a>


<div class="code"></div>

```cpp

HRESULT hr;
ITfMessagePump *pMessagePump;

hr = pThreadManager->QueryInterface(IID_ITfMessagePump, (LPVOID*)&pMessagePump);
if(SUCCEEDED(hr))
{
    //Use the ITfMessagePump interface. 
    
    //Release the ITfMessagePump interface. 
    pMessagePump->Release();
}

```
