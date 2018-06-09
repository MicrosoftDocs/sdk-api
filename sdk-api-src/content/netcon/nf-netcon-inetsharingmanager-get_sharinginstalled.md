---
UID: NF:netcon.INetSharingManager.get_SharingInstalled
title: INetSharingManager::get_SharingInstalled
author: windows-sdk-content
description: Reports whether the currently-installed version of Windows XP supports connection sharing.
old-location: ics\inetsharingmanager_get_sharinginstalled.htm
old-project: ICS
ms.assetid: 7cf705dd-41c3-4ac7-a75f-5677a7b49645
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: INetSharingManager interface [ICS/ICF],get_SharingInstalled method, INetSharingManager.get_SharingInstalled, INetSharingManager::get_SharingInstalled, _ics_inetsharingmanager_get_sharinginstalled, get_SharingInstalled, get_SharingInstalled method [ICS/ICF], get_SharingInstalled method [ICS/ICF],INetSharingManager interface, ics.inetsharingmanager_get_sharinginstalled, netcon/INetSharingManager::get_SharingInstalled
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: netcon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SHARINGCONNECTIONTYPE, *LPSHARINGCONNECTIONTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Hnetcfg.dll
api_name:
 - INetSharingManager.get_SharingInstalled
product: Windows
targetos: Windows
req.lib: 
req.dll: Hnetcfg.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetSharingManager::get_SharingInstalled


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The 
<b>get_SharingInstalled</b> method reports whether the currently-installed version of Windows XP supports connection sharing.


## -parameters




### -param pbInstalled [out]

A pointer to a <b>VARIANT_BOOL</b> that specifies whether the currently-installed version Windows XP supports connection sharing. For more information, see Remarks.


## -returns



If the method succeeds the return value is S_OK.

If the method fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The operation was aborted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
A specified interface is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
A specified method is not implemented.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate required memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A pointer passed as a parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for unknown reasons.

</td>
</tr>
</table>
 




## -remarks



This method sets the <i>pbInstalled</i> parameter to <b>TRUE</b> when called on the following versions of Windows XP:

<ul>
<li>Windows XP Home Edition</li>
<li>Windows XP Professional</li>
<li>Windows XP Embedded</li>
</ul>
This function sets the <i>pbInstalled</i> parameter to <b>FALSE</b> when called on other versions of Windows XP.

To determine whether sharing is enable for a particular connection, call 
<a href="https://msdn.microsoft.com/b8872235-0ef3-4ade-8085-fd90f40549af">INetSharingConfiguration::get_SharingEnabled</a> method for that connection.




## -see-also




<a href="https://msdn.microsoft.com/e7009d13-89c2-4fd9-8f6c-dcdc67178598">INetSharingManager</a>



<a href="https://msdn.microsoft.com/dfef918e-9abf-4ac2-8365-28cd5b249add">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

