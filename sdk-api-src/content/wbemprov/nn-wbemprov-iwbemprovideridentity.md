---
UID: NN:wbemprov.IWbemProviderIdentity
title: IWbemProviderIdentity
author: windows-sdk-content
description: The IWbemProviderIdentity interface is implemented by an event provider if the provider registers itself using more than one Name (multiple instances of __Win32Provider) with the same CLSID value.
old-location: wmi\iwbemprovideridentity.htm
old-project: WmiSdk
ms.assetid: 872daa72-c6ff-4c6d-a870-c32e3688eb13
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWbemProviderIdentity, IWbemProviderIdentity interface [Windows Management Instrumentation], IWbemProviderIdentity interface [Windows Management Instrumentation],described, _hmm_iwbemprovideridentity, wbemprov/IWbemProviderIdentity, wmi.iwbemprovideridentity
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wbemprov.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemsvc.dll
api_name:
 - IWbemProviderIdentity
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Wbemsvc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemProviderIdentity interface


## -description


The 
<b>IWbemProviderIdentity</b> interface is implemented by an event provider if the provider registers itself using more than one 
<b>Name</b> (multiple instances of 
<a href="https://msdn.microsoft.com/41e0d938-00c6-4f4c-8027-8b8512398dee">__Win32Provider</a>) with the same <a href="https://msdn.microsoft.com/en-us/library/ms688628(v=VS.85).aspx">CLSID</a> value. The class provides a mechanism for distinguishing which named provider should be used.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemProviderIdentity</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWbemProviderIdentity</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemProviderIdentity</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e600d562-6a93-422c-88f2-d44196191843">SetRegistrationObject</a>
</td>
<td align="left" width="63%">
Sets the provider object for this registration.

</td>
</tr>
</table> 

