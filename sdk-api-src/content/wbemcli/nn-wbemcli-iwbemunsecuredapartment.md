---
UID: NN:wbemcli.IWbemUnsecuredApartment
title: IWbemUnsecuredApartment (wbemcli.h)
description: Allows client applications to determine whether Unsecapp.exe performs access checks on asynchronous callbacks.
helpviewer_keywords: ["IWbemUnsecuredApartment","IWbemUnsecuredApartment interface [Windows Management Instrumentation]","IWbemUnsecuredApartment interface [Windows Management Instrumentation]","described","wbemcli/IWbemUnsecuredApartment","wmi.iwbemunsecuredapartment"]
old-location: wmi\iwbemunsecuredapartment.htm
tech.root: wmi
ms.assetid: e77a9ea0-a4cc-4e86-8506-414ecced88f2
ms.date: 12/05/2018
ms.keywords: IWbemUnsecuredApartment, IWbemUnsecuredApartment interface [Windows Management Instrumentation], IWbemUnsecuredApartment interface [Windows Management Instrumentation],described, wbemcli/IWbemUnsecuredApartment, wmi.iwbemunsecuredapartment
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemUnsecuredApartment
 - wbemcli/IWbemUnsecuredApartment
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Unsecapp.exe
api_name:
 - IWbemUnsecuredApartment
---

# IWbemUnsecuredApartment interface


## -description

The <b>IWbemUnsecuredApartment</b> interface 
   allows client applications to determine whether Unsecapp.exe performs access 
   checks on asynchronous callbacks. Unsecapp.exe supports both 
   <a href="/windows/desktop/api/wbemcli/nn-wbemcli-iunsecuredapartment">IUnsecuredApartment</a> and 
   <b>IWbemUnsecuredApartment</b> interfaces.

## -inheritance

The <b>IWbemUnsecuredApartment</b> interface inherits from <b>IUnsecuredApartment</b>. <b>IWbemUnsecuredApartment</b> also has these types of members:

## -remarks

<b>IWbemUnsecuredApartment</b> is similar to 
     <a href="/windows/desktop/api/wbemcli/nn-wbemcli-iunsecuredapartment">IUnsecuredApartment</a>, which also creates a sink in a 
     separate process. For more information, see 
     <a href="/windows/desktop/WmiSdk/performing-access-checks">Performing Access Checks</a>.


<b>HKEY_LOCAL_MACHINE</b>&#92;<b>SOFTWARE</b>&#92;<b>Microsoft</b>&#92;<b>WBEM</b>&#92;<b>CIMOM</b>&#92;<b>UnsecAppAccessControlDefault</b>

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iunsecuredapartment">IUnsecuredApartment</a>



<a href="/windows/desktop/WmiSdk/lowering-the-security-for-a-sink-in-a-separate-process">Lowering the Security for a Sink in a Separate Process</a>



<a href="/windows/desktop/WmiSdk/performing-access-checks">Performing Access Checks</a>



<a href="/windows/desktop/WmiSdk/setting-security-on-an-asynchronous-call">Setting Security on an Asynchronous Call</a>
