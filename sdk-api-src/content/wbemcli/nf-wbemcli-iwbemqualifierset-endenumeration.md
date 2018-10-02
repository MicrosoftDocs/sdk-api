---
UID: NF:wbemcli.IWbemQualifierSet.EndEnumeration
title: IWbemQualifierSet::EndEnumeration
author: windows-sdk-content
description: Call the IWbemQualifierSet::EndEnumeration method when you plan to terminate enumerations initiated with IWbemQualifierSet::BeginEnumeration and IWbemQualifierSet::Next.
old-location: wmi\iwbemqualifierset_endenumeration.htm
tech.root: WmiSdk
ms.assetid: 317409e9-b098-404b-bc09-78b5b5ae7fc7
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: EndEnumeration, EndEnumeration method [Windows Management Instrumentation], EndEnumeration method [Windows Management Instrumentation],IWbemQualifierSet interface, IWbemQualifierSet interface [Windows Management Instrumentation],EndEnumeration method, IWbemQualifierSet.EndEnumeration, IWbemQualifierSet::EndEnumeration, _hmm_iwbemqualifierset_endenumeration, wbemcli/IWbemQualifierSet::EndEnumeration, wmi.iwbemqualifierset_endenumeration
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wbemcli.h
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
req.dll: Fastprox.dll; Krnlprov.dll; Ncprov.dll; Wbemcore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fastprox.dll
 - Krnlprov.dll
 - Ncprov.dll
 - Wbemcore.dll
api_name:
 - IWbemQualifierSet.EndEnumeration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemQualifierSet::EndEnumeration


## -description


Call the 
<b>IWbemQualifierSet::EndEnumeration</b> method when you plan to terminate enumerations initiated with 
<a href="https://msdn.microsoft.com/57fa60d1-54d2-412d-b39b-c35dfd709d0c">IWbemQualifierSet::BeginEnumeration</a> and 
<a href="https://msdn.microsoft.com/76afa293-1bd9-442b-bc9b-2247459bd49c">IWbemQualifierSet::Next</a>. This call is recommended, but not required. It immediately releases resources associated with the enumeration.


## -parameters






## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>.




## -see-also




<a href="https://msdn.microsoft.com/8b36bd32-4931-4641-a019-cbaa3547edd0">IWbemQualifierSet</a>



<a href="https://msdn.microsoft.com/57fa60d1-54d2-412d-b39b-c35dfd709d0c">IWbemQualifierSet::BeginEnumeration</a>



<a href="https://msdn.microsoft.com/76afa293-1bd9-442b-bc9b-2247459bd49c">IWbemQualifierSet::Next</a>
 

 

