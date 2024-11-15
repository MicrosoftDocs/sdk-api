---
UID: NS:richedit._editstream
title: EDITSTREAM (richedit.h)
description: Contains information that an application passes to a rich edit control in a EM_STREAMIN or EM_STREAMOUT message. The rich edit control uses the information to transfer a stream of data into or out of the control.
helpviewer_keywords: ["EDITSTREAM","EDITSTREAM structure [Windows Controls]","_win32_EDITSTREAM_str","_win32_EDITSTREAM_str_cpp","controls.EDITSTREAM","controls._win32_EDITSTREAM_str","richedit/EDITSTREAM"]
old-location: controls\EDITSTREAM.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\editstream.htm
ms.date: 12/05/2018
ms.keywords: EDITSTREAM, EDITSTREAM structure [Windows Controls], _win32_EDITSTREAM_str, _win32_EDITSTREAM_str_cpp, controls.EDITSTREAM, controls._win32_EDITSTREAM_str, richedit/EDITSTREAM
req.header: richedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: EDITSTREAM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _editstream
 - richedit/_editstream
 - EDITSTREAM
 - richedit/EDITSTREAM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Richedit.h
api_name:
 - EDITSTREAM
---

# EDITSTREAM structure


## -description

Contains information that an application passes to a rich edit control in a <a href="/windows/win32/controls/em-streamin">EM_STREAMIN</a> or <a href="/windows/win32/controls/em-streamout">EM_STREAMOUT</a> message. The rich edit control uses the information to transfer a stream of data into or out of the control.

## -struct-fields

### -field dwCookie

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD_PTR</a></b>

Specifies an application-defined value that the rich edit control passes to the <a href="/windows/win32/api/richedit/nc-richedit-editstreamcallback">EditStreamCallback</a> callback function specified by the <b>pfnCallback</b> member.

### -field dwError

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Indicates the results of the stream-in (read) or stream-out (write) operation. A value of zero indicates no error. A nonzero value can be the return value of the <a href="/windows/win32/api/richedit/nc-richedit-editstreamcallback">EditStreamCallback</a> function or a code indicating that the control encountered an error.

### -field pfnCallback

Type: <b>EDITSTREAMCALLBACK</b>

Pointer to an <a href="/windows/win32/api/richedit/nc-richedit-editstreamcallback">EditStreamCallback</a> function, which is an application-defined function that the control calls to transfer data. The control calls the callback function repeatedly, transferring a portion of the data with each call.

## -see-also

<a href="/windows/win32/controls/em-streamin">EM_STREAMIN</a>



<a href="/windows/win32/controls/em-streamout">EM_STREAMOUT</a>



<a href="/windows/win32/api/richedit/nc-richedit-editstreamcallback">EditStreamCallback</a>



<b>Reference</b>
