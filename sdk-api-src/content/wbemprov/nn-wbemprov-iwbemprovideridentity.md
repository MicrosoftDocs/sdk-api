---
UID: NN:wbemprov.IWbemProviderIdentity
title: IWbemProviderIdentity (wbemprov.h)
description: The IWbemProviderIdentity interface is implemented by an event provider if the provider registers itself using more than one Name (multiple instances of __Win32Provider) with the same CLSID value.
old-location: wmi\iwbemprovideridentity.htm
tech.root: WmiSdk
ms.assetid: 872daa72-c6ff-4c6d-a870-c32e3688eb13
ms.date: 12/05/2018
ms.keywords: IWbemProviderIdentity, IWbemProviderIdentity interface [Windows Management Instrumentation], IWbemProviderIdentity interface [Windows Management Instrumentation],described, _hmm_iwbemprovideridentity, wbemprov/IWbemProviderIdentity, wmi.iwbemprovideridentity
f1_keywords:
- wbemprov/IWbemProviderIdentity
dev_langs:
- c++
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
req.lib: Wbemuuid.lib
req.dll: Wbemsvc.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wbemsvc.dll
api_name:
- IWbemProviderIdentity
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWbemProviderIdentity interface


## -description


The 
<b>IWbemProviderIdentity</b> interface is implemented by an event provider if the provider registers itself using more than one 
<b>Name</b> (multiple instances of 
<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/--win32provider">__Win32Provider</a>) with the same <a href="https://docs.microsoft.com/windows/desktop/com/clsid">CLSID</a> value. The class provides a mechanism for distinguishing which named provider should be used.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemProviderIdentity</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemProviderIdentity</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wbemprov/nf-wbemprov-iwbemprovideridentity-setregistrationobject">SetRegistrationObject</a>
</td>
<td align="left" width="63%">
Sets the provider object for this registration.

</td>
</tr>
</table> 

