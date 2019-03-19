---
UID: NF:netcon.INetSharingManager.get_INetSharingConfigurationForINetConnection
title: INetSharingManager::get_INetSharingConfigurationForINetConnection (netcon.h)
author: windows-sdk-content
description: The get_INetSharingConfigurationForINetConnection method retrieves an INetSharingConfiguration interface for the specified connection.
old-location: ics\inetsharingmanager_get_inetsharingconfigurationforinetconnection.htm
tech.root: ics
ms.assetid: 8f774509-0efb-49e5-bf56-61f4810631bd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: INetSharingManager interface [ICS/ICF],get_INetSharingConfigurationForINetConnection method, INetSharingManager.get_INetSharingConfigurationForINetConnection, INetSharingManager::get_INetSharingConfigurationForINetConnection, _ics_inetsharingmanager_get_inetsharingconfigurationforinetconnection, get_INetSharingConfigurationForINetConnection, get_INetSharingConfigurationForINetConnection method [ICS/ICF], get_INetSharingConfigurationForINetConnection method [ICS/ICF],INetSharingManager interface, ics.inetsharingmanager_get_inetsharingconfigurationforinetconnection, netcon/INetSharingManager::get_INetSharingConfigurationForINetConnection
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
req.lib: 
req.dll: Hnetcfg.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Hnetcfg.dll
api_name:
 - INetSharingManager.get_INetSharingConfigurationForINetConnection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetSharingManager::get_INetSharingConfigurationForINetConnection


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/en-us/library/Aa366453(v=VS.85).aspx">Windows Firewall API</a>.]

The 
<b>get_INetSharingConfigurationForINetConnection</b> method retrieves an 
<a href="https://msdn.microsoft.com/en-us/library/Aa365935(v=VS.85).aspx">INetSharingConfiguration</a> interface for the specified connection.


## -parameters




### -param pNetConnection

Pointer to an 
<a href="https://msdn.microsoft.com/7dd55645-c8e6-4ebd-9bf6-3bc3b3f5166f">INetConnection</a> interface for an Internet connection.
					


### -param ppNetSharingConfiguration [out]

Pointer to an interface pointer that, on successful return, points to an 
<a href="https://msdn.microsoft.com/en-us/library/Aa365935(v=VS.85).aspx">INetSharingConfiguration</a> interface for the connection specified by the <i>pNetConnection</i> parameter.


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
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa365960(v=VS.85).aspx">INetSharingManager</a>



<a href="https://msdn.microsoft.com/dfef918e-9abf-4ac2-8365-28cd5b249add">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa366131(v=VS.85).aspx">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

