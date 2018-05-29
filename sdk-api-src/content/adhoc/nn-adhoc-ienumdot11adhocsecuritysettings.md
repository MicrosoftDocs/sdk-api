---
UID: NN:adhoc.IEnumDot11AdHocSecuritySettings
title: IEnumDot11AdHocSecuritySettings
author: windows-sdk-content
description: Represents the collection of security settings associated with each visible wireless ad hoc network.
old-location: nwifi\ienumdot11adhocsecuritysettings.htm
old-project: NativeWiFi
ms.assetid: 137abd1b-997d-4003-9fef-8db56b273149
ms.author: windowssdkdev
ms.date: 04/13/2018
ms.keywords: IEnumDot11AdHocSecuritySettings, IEnumDot11AdHocSecuritySettings interface [NativeWIFI], IEnumDot11AdHocSecuritySettings interface [NativeWIFI],described, adhoc/IEnumDot11AdHocSecuritySettings, nwifi.ienumdot11adhocsecuritysettings
ms.prod: windows
ms.technology: windows-sdk
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
-	IEnumDot11AdHocSecuritySettings
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IEnumDot11AdHocSecuritySettings interface


## -description


This interface represents the collection of security settings associated with each visible wireless ad hoc network.  It is a standard enumerator.
<div class="alert"><b>Note</b>  Ad hoc mode might not be available in future versions of Windows. Starting with Windows 8.1 and Windows Server 2012 R2, use <a href="https://msdn.microsoft.com/library/windows/hardware/mt244265">Wi-Fi Direct</a> instead.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumDot11AdHocSecuritySettings</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumDot11AdHocSecuritySettings</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumDot11AdHocSecuritySettings</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27ef4cab-9aa5-4aa2-9e2e-fb16aae99045">IEnumDot11AdHocSecuritySettings::Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumeration interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77101f70-de5d-4db9-a59d-5b07f386c0b7">IEnumDot11AdHocSecuritySettings::Next</a>
</td>
<td align="left" width="63%">
Gets the specified number of elements from the sequence and advances the current position by the number of items retrieved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15fc655c-56d3-4f1e-b4e9-cb0e16191dc7">IEnumDot11AdHocSecuritySettings::Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c423e794-bb3a-4dd8-b6bc-324d91909e92">IEnumDot11AdHocSecuritySettings::Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 

