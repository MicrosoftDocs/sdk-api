---
UID: NN:msctf.ITfThreadMgr2
title: ITfThreadMgr2 (msctf.h)
description: The ITfThreadMgr2 defines the primary object implemented by the TSF manager. ITfThreadMgr2 is used by applications and text services to activate and deactivate text services, create document managers, and maintain the document context focus.
helpviewer_keywords: ["ITfThreadMgr2","ITfThreadMgr2 interface [Text Services Framework]","ITfThreadMgr2 interface [Text Services Framework]","described","msctf/ITfThreadMgr2","tsf.itfthreadmgr2"]
old-location: tsf\itfthreadmgr2.htm
tech.root: TSF
ms.assetid: B80A0DBA-349A-450D-BD9D-14BD36308590
ms.date: 12/05/2018
ms.keywords: ITfThreadMgr2, ITfThreadMgr2 interface [Text Services Framework], ITfThreadMgr2 interface [Text Services Framework],described, msctf/ITfThreadMgr2, tsf.itfthreadmgr2
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITfThreadMgr2
 - msctf/ITfThreadMgr2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.h
api_name:
 - ITfThreadMgr2
---

# ITfThreadMgr2 interface


## -description

The <b>ITfThreadMgr2</b> defines the primary object implemented by the TSF manager. <b>ITfThreadMgr2</b> is used by applications and text services to activate and deactivate text services, create document managers, and maintain the document context focus.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfThreadMgr2</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfThreadMgr2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfThreadMgr2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr2-activate">Activate</a>
</td>
<td align="left" width="63%">
 Activates TSF for the calling thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr2-activateex">ActivateEx</a>
</td>
<td align="left" width="63%">
Initializes and activates TSF for the calling thread with a flag that specifies how TSF is activated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr2-createdocumentmgr">CreateDocumentMgr</a>
</td>
<td align="left" width="63%">
Creates a document manager object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr2-deactivate">Deactivate</a>
</td>
<td align="left" width="63%">
Deactivates TSF for the calling thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr2-enumdocumentmgrs">EnumDocumentMgrs</a>
</td>
<td align="left" width="63%">
Returns an enumerator for all the document managers within the calling thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr2-enumfunctionproviders">EnumFunctionProviders</a>
</td>
<td align="left" width="63%">
Obtains an enumerator for all of the function providers registered for the calling thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr2-getactiveflags">GetActiveFlags</a>
</td>
<td align="left" width="63%">
Gets the active flags of the calling thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr2-getfocus">GetFocus</a>
</td>
<td align="left" width="63%">
Returns the document manager that has the input focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr2-getfunctionprovider">GetFunctionProvider</a>
</td>
<td align="left" width="63%">
 Obtains the specified function provider object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr2-getglobalcompartment">GetGlobalCompartment</a>
</td>
<td align="left" width="63%">
Obtains the global compartment manager object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr2-isthreadfocus">IsThreadFocus</a>
</td>
<td align="left" width="63%">
Determines if the calling thread has the TSF input focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr2-resumekeystrokehandling">ResumeKeystrokeHandling</a>
</td>
<td align="left" width="63%">
Resumes suspended keystroke handling.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr2-setfocus">SetFocus</a>
</td>
<td align="left" width="63%">
Sets the input focus to the specified document manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr2-suspendkeystrokehandling">SuspendKeystrokeHandling</a>
</td>
<td align="left" width="63%">
Suspends handling keystrokes.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>

