---
UID: NN:wbemcli.IWbemUnsecuredApartment
title: IWbemUnsecuredApartment (wbemcli.h)
author: windows-sdk-content
description: Allows client applications to determine whether Unsecapp.exe performs access checks on asynchronous callbacks.
old-location: wmi\iwbemunsecuredapartment.htm
tech.root: WmiSdk
ms.assetid: e77a9ea0-a4cc-4e86-8506-414ecced88f2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWbemUnsecuredApartment, IWbemUnsecuredApartment interface [Windows Management Instrumentation], IWbemUnsecuredApartment interface [Windows Management Instrumentation],described, wbemcli/IWbemUnsecuredApartment, wmi.iwbemunsecuredapartment
ms.topic: interface
f1_keywords: 
 - "wbemcli/IWbemUnsecuredApartment"
dev_langs:
 - c++
req.header: wbemcli.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.dll: Unsecapp.exe
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Unsecapp.exe
api_name:
 - IWbemUnsecuredApartment
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWbemUnsecuredApartment interface


## -description


The <b>IWbemUnsecuredApartment</b> interface 
   allows client applications to determine whether Unsecapp.exe performs access 
   checks on asynchronous callbacks. Unsecapp.exe supports both 
   <a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nn-wbemcli-iunsecuredapartment">IUnsecuredApartment</a> and 
   <b>IWbemUnsecuredApartment</b> interfaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemUnsecuredApartment</b> interface inherits from <b>IUnsecuredApartment</b>. <b>IWbemUnsecuredApartment</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemUnsecuredApartment</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub">CreateSinkStub</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub">CreateSinkStub</a> method is 
     similar to the 
     <a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub">IUnsecuredApartment::CreateObjectStub</a> 
     method. It creates an object forwarder sink and performs access checks for receiving asynchronous calls from 
     WMI.

</td>
</tr>
</table> 


## -remarks



<b>IWbemUnsecuredApartment</b> is similar to 
     <a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nn-wbemcli-iunsecuredapartment">IUnsecuredApartment</a>, which also creates a sink in a 
     separate process. For more information, see 
     <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/performing-access-checks">Performing Access Checks</a>.


<b>HKEY_LOCAL_MACHINE</b>\<b>SOFTWARE</b>\<b>Microsoft</b>\<b>WBEM</b>\<b>CIMOM</b>\<b>UnsecAppAccessControlDefault</b>






## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nn-wbemcli-iunsecuredapartment">IUnsecuredApartment</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/lowering-the-security-for-a-sink-in-a-separate-process">Lowering the Security for a Sink in a Separate Process</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/performing-access-checks">Performing Access Checks</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/setting-security-on-an-asynchronous-call">Setting Security on an Asynchronous Call</a>
 

 

