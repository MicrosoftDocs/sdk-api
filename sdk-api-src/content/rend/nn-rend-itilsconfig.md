---
UID: NN:rend.ITILSConfig
title: ITILSConfig (rend.h)
author: windows-sdk-content
description: The ITILSConfig interface allows configuration of the ILS directory.
old-location: tapi3\itilsconfig.htm
tech.root: Tapi
ms.assetid: 92a5624b-acf5-4280-9932-860fde53c6a0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITILSConfig, ITILSConfig interface [TAPI 2.2], ITILSConfig interface [TAPI 2.2],described, _tapi3_itilsconfig, rend/ITILSConfig, tapi3.itilsconfig
ms.topic: interface
f1_keywords: 
 - "rend/ITILSConfig"
req.header: rend.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rend.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Rend.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Rend.dll
api_name:
 - ITILSConfig
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITILSConfig interface


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>ITILSConfig</b> interface allows configuration of the ILS directory. This interface is available only on Directory objects that return DT_ILS from 
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectory-get_directorytype">ITDirectory::get_DirectoryType</a>. The 
<b>ITILSConfig</b> interface is created by calling <b>QueryInterface</b> on 
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nn-rend-itdirectory">ITDirectory</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITILSConfig</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITILSConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITILSConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itilsconfig-get_port">get_Port</a>
</td>
<td align="left" width="63%">
Gets the port number used to connect to the server of a given ILS directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itilsconfig-put_port">put_Port</a>
</td>
<td align="left" width="63%">
Sets the port number used to connect to the server of a given ILS directory.

</td>
</tr>
</table> 

