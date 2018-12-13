---
UID: NN:msctf.ITfThreadMgr2
title: ITfThreadMgr2
author: windows-sdk-content
description: The ITfThreadMgr2 defines the primary object implemented by the TSF manager. ITfThreadMgr2 is used by applications and text services to activate and deactivate text services, create document managers, and maintain the document context focus.
old-location: tsf\itfthreadmgr2.htm
tech.root: TSF
ms.assetid: B80A0DBA-349A-450D-BD9D-14BD36308590
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITfThreadMgr2, ITfThreadMgr2 interface [Text Services Framework], ITfThreadMgr2 interface [Text Services Framework],described, msctf/ITfThreadMgr2, tsf.itfthreadmgr2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.h
api_name:
 - ITfThreadMgr2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITfThreadMgr2 interface


## -description


The <b>ITfThreadMgr2</b> defines the primary object implemented by the TSF manager. <b>ITfThreadMgr2</b> is used by applications and text services to activate and deactivate text services, create document managers, and maintain the document context focus.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfThreadMgr2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfThreadMgr2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/FD1548F5-15F6-4BBC-A7D1-B0F4B881D9F8">Activate</a>
</td>
<td align="left" width="63%">
 Activates TSF for the calling thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ADA34C7-6BE8-4719-B220-1F0E5F466178">ActivateEx</a>
</td>
<td align="left" width="63%">
Initializes and activates TSF for the calling thread with a flag that specifies how TSF is activated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4B19EA80-9F42-4FFF-AB3D-4D0B5B2174F8">CreateDocumentMgr</a>
</td>
<td align="left" width="63%">
Creates a document manager object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ED1A430-27C3-44BA-BF17-B5FB9D4C7087">Deactivate</a>
</td>
<td align="left" width="63%">
Deactivates TSF for the calling thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16A07BA6-05C2-4CA6-97D6-F1B4CEE1E757">EnumDocumentMgrs</a>
</td>
<td align="left" width="63%">
Returns an enumerator for all the document managers within the calling thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0F28BDFD-4CD8-4D50-92D9-6A60B80122B2">EnumFunctionProviders</a>
</td>
<td align="left" width="63%">
Obtains an enumerator for all of the function providers registered for the calling thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F0777E69-C9E2-4E40-9CE0-56084D1C8A41">GetActiveFlags</a>
</td>
<td align="left" width="63%">
Gets the active flags of the calling thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A4106774-1817-4308-BD7E-C303AED2B576">GetFocus</a>
</td>
<td align="left" width="63%">
Returns the document manager that has the input focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4B2B2098-ECA1-454F-8F7F-978893C466F7">GetFunctionProvider</a>
</td>
<td align="left" width="63%">
 Obtains the specified function provider object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AC1D27C5-C9D9-4658-AC3C-9C3A723F8597">GetGlobalCompartment</a>
</td>
<td align="left" width="63%">
Obtains the global compartment manager object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8440BEE8-865F-4403-8558-C77638290A7F">IsThreadFocus</a>
</td>
<td align="left" width="63%">
Determines if the calling thread has the TSF input focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/68948ACE-EF49-4F24-B579-72304A00A98D">ResumeKeystrokeHandling</a>
</td>
<td align="left" width="63%">
Resumes suspended keystroke handling.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62BC0797-668D-4CA1-8313-338FF7F40D89">SetFocus</a>
</td>
<td align="left" width="63%">
Sets the input focus to the specified document manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98E0D017-F0A2-4F80-9CD3-16D22170BFDF">SuspendKeystrokeHandling</a>
</td>
<td align="left" width="63%">
Suspends handling keystrokes.

</td>
</tr>
</table> 


## -see-also




<a href="_COM_IUnknown">IUnknown</a>
 

 

