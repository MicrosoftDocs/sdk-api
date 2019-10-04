---
UID: NN:wsmandisp.IWSManEx2
title: IWSManEx2 (wsmandisp.h)
author: windows-sdk-content
description: Extends the methods and properties of the IWSManEx interface to include a method that returns a session flag value related to authentication using client certificates.
old-location: winrm\iwsmanex2.htm
tech.root: winrm
ms.assetid: 4c398e10-3822-4042-8a43-1d7889ae6cac
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWSManEx2, IWSManEx2 interface [Windows Remote Management], IWSManEx2 interface [Windows Remote Management],described, winrm.iwsmanex2, wsmandisp/IWSManEx2
ms.topic: interface
f1_keywords: 
 - "wsmandisp/IWSManEx2"
dev_langs:
 - c++
req.header: wsmandisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WSManDisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - IWSManEx2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSManEx2 interface


## -description


Extends the methods and properties of the <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanex">IWSManEx</a> interface to include a method that returns a session flag value related to authentication using client certificates.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSManEx2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanex">IWSManEx</a>. <b>IWSManEx2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSManEx2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanex2-sessionflaguseclientcertificate">IWSManEx2::SessionFlagUseClientCertificate</a>
</td>
<td align="left" width="63%">
Returns the value of the authentication flag <b>WSManFlagUseClientCertificate</b>.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanex">IWSManEx</a>
 

 

