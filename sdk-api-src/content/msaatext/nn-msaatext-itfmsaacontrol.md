---
UID: NN:msaatext.ITfMSAAControl
title: ITfMSAAControl
author: windows-sdk-content
description: The ITfMSAAControl interface is used by Microsoft Active Accessibility to add or remove a document from TSF control, to avoid unnecessary overhead in TSF. This interface is not recommended for use by other applications.
old-location: tsf\itfmsaacontrol.htm
old-project: TSF
ms.assetid: e01a0177-7e3a-4087-84b8-151da2145be8
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: ITfMSAAControl, ITfMSAAControl interface [Text Services Framework], ITfMSAAControl interface [Text Services Framework],described, msaatext/ITfMSAAControl, tsf.itfmsaacontrol
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msaatext.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MSAAText.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SSTP_CONFIG_PARAMS, *PSSTP_CONFIG_PARAMS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITfMSAAControl
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfMSAAControl interface


## -description


The <b>ITfMSAAControl</b> interface is used by <a href="_msaa_microsoft_active_accessibility_start_page">Microsoft Active Accessibility</a> to add or remove a document from TSF control, to avoid unnecessary overhead in TSF. This interface is not recommended for use by other applications.

The interface ID is IID_ITfMSAAControl.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfMSAAControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfMSAAControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfMSAAControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/344cabbb-286e-415d-980f-349fb637a78d">SystemDisableMSAA</a>
</td>
<td align="left" width="63%">
Used by MSAA to halt TSF support of an MSAA client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fec3aa3f-3554-4c21-9557-a12388d97a94">SystemEnableMSAA</a>
</td>
<td align="left" width="63%">
Used by MSAA to request TSF support of an MSAA client.

</td>
</tr>
</table> 


## -see-also




<a href="_COM_IUnknown">IUnknown</a>



<a href="_msaa_microsoft_active_accessibility_start_page">Microsoft Active Accessibility</a>
 

 

