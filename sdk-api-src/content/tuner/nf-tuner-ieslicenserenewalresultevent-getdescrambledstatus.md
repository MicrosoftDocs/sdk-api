---
UID: NF:tuner.IESLicenseRenewalResultEvent.GetDescrambledStatus
title: IESLicenseRenewalResultEvent::GetDescrambledStatus
author: windows-driver-content
description: Gets a code from a LicenseRenewalResult event that indicates the result of an attempt to descramble protected content.
old-location: mstv\ieslicenserenewalresultevent_getdescrambledstatus.htm
old-project: mstv
ms.assetid: ed09aea2-e000-40ce-bd94-a174e75a5001
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetDescrambledStatus, GetDescrambledStatus method [DirectShow], GetDescrambledStatus method [DirectShow],IESLicenseRenewalResultEvent interface, IESLicenseRenewalResultEvent interface [DirectShow],GetDescrambledStatus method, IESLicenseRenewalResultEvent.GetDescrambledStatus, IESLicenseRenewalResultEvent::GetDescrambledStatus, mstv.ieslicenserenewalresultevent_getdescrambledstatus, tuner/IESLicenseRenewalResultEvent::GetDescrambledStatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IESLicenseRenewalResultEvent.GetDescrambledStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IESLicenseRenewalResultEvent::GetDescrambledStatus


## -description


Gets a code  from a  <a href="https://msdn.microsoft.com/6f9cbec4-7934-41fc-b387-3f45aa273a72">LicenseRenewalResult</a> event that indicates the result of an attempt to descramble protected content.


## -parameters




### -param pDescrambledStatus [out, retval]


            Receives a status code that indicates the descrambling status. For more information, see <i>Protected Broadcast Driver Architecture, Part 1: Core Services</i>, section 5.5. This document is part of the PBDA specification, which you can download from <a href="http://go.microsoft.com/fwlink/p/?linkid=132926">http://go.microsoft.com/fwlink/p/?linkid=132926</a>.
          (This resource may not be available in some languages 

and countries.)

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00000000 </dt>
</dl>
</td>
<td width="60%">
Free to air content (nonprotected). 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Descrambling possible. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x80010000</dt>
</dl>
</td>
<td width="60%">
No technical (other). 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x80010001 </dt>
</dl>
</td>
<td width="60%">
(No technical) firmware upgrade required. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x80010002 </dt>
</dl>
</td>
<td width="60%">
(No technical) internal failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x80010003 </dt>
</dl>
</td>
<td width="60%">
(No technical) initializing/not ready.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x80010004 </dt>
</dl>
</td>
<td width="60%">
(No technical) setup required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x80010005 </dt>
</dl>
</td>
<td width="60%">
(No technical) no access card.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x80010006 </dt>
</dl>
</td>
<td width="60%">
(No technical) access card failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x80010007 </dt>
</dl>
</td>
<td width="60%">
(No technical) bad access card.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x80010008 </dt>
</dl>
</td>
<td width="60%">
(No technical) wrong access card.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x80010009 </dt>
</dl>
</td>
<td width="60%">
(No technical) expired access card.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x8001000A</dt>
</dl>
</td>
<td width="60%">
(No technical) out of resources, for example, too many streams.	

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x8001000B </dt>
</dl>
</td>
<td width="60%">
(No technical) not in purchase window.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x8001000C </dt>
</dl>
</td>
<td width="60%">
(No technical) not in purchase window, prior.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x8001000D </dt>
</dl>
</td>
<td width="60%">
(No technical) not in purchase window, after.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x80020000 </dt>
</dl>
</td>
<td width="60%">
No entitlement (other).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x80020001</dt>
</dl>
</td>
<td width="60%">
(No entitlement) access card not authorized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x80020002</dt>
</dl>
</td>
<td width="60%">
(No entitlement) service not authorized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x80020003</dt>
</dl>
</td>
<td width="60%">
(No entitlement) service expired.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x80020004</dt>
</dl>
</td>
<td width="60%">
(No entitlement) account not authorized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x80020005</dt>
</dl>
</td>
<td width="60%">
(No entitlement) account expired.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x80020006</dt>
</dl>
</td>
<td width="60%">
(No entitlement) service blacked out.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x80020007</dt>
</dl>
</td>
<td width="60%">
(No entitlement) purchase required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x80020008</dt>
</dl>
</td>
<td width="60%">
(No entitlement) insufficient credit.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x80020009</dt>
</dl>
</td>
<td width="60%">
(No entitlement) purchase canceled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x8002000A</dt>
</dl>
</td>
<td width="60%">
(No entitlement) renewal entitlement expired.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x8002000B</dt>
</dl>
</td>
<td width="60%">
(No entitlement) showing not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x8002000C</dt>
</dl>
</td>
<td width="60%">
(No entitlement) showing next.

</td>
</tr>
</table>
 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6f9cbec4-7934-41fc-b387-3f45aa273a72">IESLicenseRenewalResultEvent</a>
 

 

