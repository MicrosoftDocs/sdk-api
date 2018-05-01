---
UID: NN:adhoc.IDot11AdHocSecuritySettings
title: IDot11AdHocSecuritySettings
author: windows-driver-content
description: Specifies the security settings for a wireless ad hoc network.
old-location: nwifi\idot11adhocsecuritysettings.htm
old-project: NativeWiFi
ms.assetid: 55b78a98-ad25-4646-b325-73d770d602b3
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: IDot11AdHocSecuritySettings, IDot11AdHocSecuritySettings interface [NativeWIFI], IDot11AdHocSecuritySettings interface [NativeWIFI], described, adhoc/IDot11AdHocSecuritySettings, nwifi.idot11adhocsecuritysettings
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: adhoc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Adhoc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DOT11_ADHOC_NETWORK_CONNECTION_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	adhoc.h
api_name:
-	IDot11AdHocSecuritySettings
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDot11AdHocSecuritySettings interface


## -description


The <b>IDot11AdHocSecuritySettings</b> interface specifies the security settings for a wireless ad hoc network. 
<div class="alert"><b>Note</b>  Ad hoc mode might not be available in future versions of Windows. Starting with Windows 8.1 and Windows Server 2012 R2, use <a href="https://msdn.microsoft.com/library/windows/hardware/mt244265">Wi-Fi Direct</a> instead.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDot11AdHocSecuritySettings</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDot11AdHocSecuritySettings</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDot11AdHocSecuritySettings</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87ba445a-1ad7-49da-aa61-ed72d118e517">IDot11AdHocSecuritySettings::GetDot11AuthAlgorithm</a>
</td>
<td align="left" width="63%">
Gets the authentication algorithm associated with the security settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46bf39e3-351f-41c2-8f68-886fce8a83bd">IDot11AdHocSecuritySettings::GetDot11CipherAlgorithm</a>
</td>
<td align="left" width="63%">
Gets the cipher algorithm associated with the security settings.

</td>
</tr>
</table> 

