---
UID: NF:wbemcli.IWbemClassObject.InheritsFrom
title: IWbemClassObject::InheritsFrom (wbemcli.h)
author: windows-sdk-content
description: The IWbemClassObject::InheritsFrom method determines if the current class or instance derives from a specified parent class.
old-location: wmi\iwbemclassobject_inheritsfrom.htm
tech.root: WmiSdk
ms.assetid: 05431e05-440e-4241-bde9-0dbd32039921
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWbemClassObject interface [Windows Management Instrumentation],InheritsFrom method, IWbemClassObject.InheritsFrom, IWbemClassObject::InheritsFrom, InheritsFrom, InheritsFrom method [Windows Management Instrumentation], InheritsFrom method [Windows Management Instrumentation],IWbemClassObject interface, _hmm_iwbemclassobject_inheritsfrom, wbemcli/IWbemClassObject::InheritsFrom, wmi.iwbemclassobject_inheritsfrom
ms.topic: method
f1_keywords: 
 - "wbemcli/IWbemClassObject.InheritsFrom"
dev_langs:
 - c++
req.header: wbemcli.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WbemCli.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WbemUuid.lib
req.dll: CIMWin32.dll; Esscli.dll; Fastprox.dll; FrameDyn.dll; FrameDynOS.dll; Krnlprov.dll; Ncprov.dll; Wbemcore.dll; Wbemess.dll; Wmipiprt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CIMWin32.dll
 - Esscli.dll
 - Fastprox.dll
 - FrameDyn.dll
 - FrameDynOS.dll
 - Krnlprov.dll
 - Ncprov.dll
 - Wbemcore.dll
 - Wbemess.dll
 - Wmipiprt.dll
api_name:
 - IWbemClassObject.InheritsFrom
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWbemClassObject::InheritsFrom


## -description


The 
<b>IWbemClassObject::InheritsFrom</b> method determines if the current class or instance derives from a specified parent class.


## -parameters




### -param strAncestor [in]

Cannot be <b>NULL</b>. It contains the class name that is being tested. If the current object has this class for one of its ancestor classes, <b>WBEM_S_NO_ERROR</b> returns. This must point to a valid <b>LPCWSTR</b>, which is treated as read-only.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">System Error Codes</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getpropertyorigin">GetPropertyOrigin</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a>
 

 

