---
UID: NN:msctf.ITfActiveLanguageProfileNotifySink
title: ITfActiveLanguageProfileNotifySink
author: windows-sdk-content
description: The ITfActiveLanguageProfileNotifySink interface is implemented by an application to receive a notification when the active language or text service changes.
old-location: tsf\itfactivelanguageprofilenotifysink.htm
tech.root: TSF
ms.assetid: c70141e8-c948-44f4-914e-454327aadf2b
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ITfActiveLanguageProfileNotifySink, ITfActiveLanguageProfileNotifySink interface [Text Services Framework], ITfActiveLanguageProfileNotifySink interface [Text Services Framework],described, _tsf_itfactivelanguageprofilenotifysink_ref, msctf/ITfActiveLanguageProfileNotifySink, tsf.itfactivelanguageprofilenotifysink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.dll: Imekrcic.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imekrcic.dll
api_name:
 - ITfActiveLanguageProfileNotifySink
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfActiveLanguageProfileNotifySink interface


## -description


The <b>ITfActiveLanguageProfileNotifySink</b> interface is implemented by an application to receive a notification when the active language or text service changes.

To install the advise sink, obtain an <a href="https://msdn.microsoft.com/2ff77f09-1b4c-4115-9bb4-4040097d1f90">ITfSource</a> object from an <a href="https://msdn.microsoft.com/3a2ba59c-3565-4f54-ac10-923dcb4882cb">ITfThreadMgr</a> object by calling <b>ITfThreadMgr::QueryInterface</b> with IID_ITfActiveLanguageProfileNotifySink. Then call <a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink</a> with IID_ITfActiveLanguageProfileNotifySink.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfActiveLanguageProfileNotifySink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfActiveLanguageProfileNotifySink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfActiveLanguageProfileNotifySink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/89444189-254e-4a3c-9c8e-79c8b96aee34">OnActivated</a>
</td>
<td align="left" width="63%">
Called when the active language or text service changes.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2ff77f09-1b4c-4115-9bb4-4040097d1f90">ITfSource
      </a>



<a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink
      </a>



<a href="https://msdn.microsoft.com/3a2ba59c-3565-4f54-ac10-923dcb4882cb">ITfThreadMgr
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

