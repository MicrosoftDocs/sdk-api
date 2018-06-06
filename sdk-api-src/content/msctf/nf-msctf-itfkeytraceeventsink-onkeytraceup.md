---
UID: NF:msctf.ITfKeyTraceEventSink.OnKeyTraceUp
title: ITfKeyTraceEventSink::OnKeyTraceUp
author: windows-sdk-content
description: ITfKeyTraceEventSink::OnKeyTraceUp method
old-location: tsf\itfkeytraceeventsink_onkeytraceup.htm
old-project: TSF
ms.assetid: 5b86de82-2c27-4824-91bb-39001b5a19e7
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: ITfKeyTraceEventSink interface [Text Services Framework],OnKeyTraceUp method, ITfKeyTraceEventSink.OnKeyTraceUp, ITfKeyTraceEventSink::OnKeyTraceUp, OnKeyTraceUp, OnKeyTraceUp method [Text Services Framework], OnKeyTraceUp method [Text Services Framework],ITfKeyTraceEventSink interface, _tsf_itfkeytraceeventsink_onkeytraceup_ref, msctf/ITfKeyTraceEventSink::OnKeyTraceUp, tsf.itfkeytraceeventsink_onkeytraceup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tiptsf.dll
api_name:
 - ITfKeyTraceEventSink.OnKeyTraceUp
product: Windows
targetos: Windows
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfKeyTraceEventSink::OnKeyTraceUp


## -description




## -parameters




### -param wParam [in]

The WPARAM of the key event. For more information about this parameter, see the <i>wParam</i> parameter in <a href="_win32_wm_keyup">WM_KEYUP</a>.


### -param lParam [in]

The LPARAM of the key event. For more information about this parameter, see the <i>lParam</i> parameter in <a href="_win32_wm_keyup">WM_KEYUP</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/29785bae-59b8-4bbb-b899-44f6fc3e83bd">ITfKeyTraceEventSink
      </a>



<a href="_win32_wm_keyup">WM_KEYUP</a>
 

 

