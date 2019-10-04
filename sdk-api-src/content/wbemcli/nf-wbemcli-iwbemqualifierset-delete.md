---
UID: NF:wbemcli.IWbemQualifierSet.Delete
title: IWbemQualifierSet::Delete (wbemcli.h)
author: windows-sdk-content
description: The IWbemQualifierSet::Delete method deletes the specified qualifier by name.
old-location: wmi\iwbemqualifierset_delete.htm
tech.root: WmiSdk
ms.assetid: 77e61fd1-a835-4ed7-8880-9eab65611ebc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Delete, Delete method [Windows Management Instrumentation], Delete method [Windows Management Instrumentation],IWbemQualifierSet interface, IWbemQualifierSet interface [Windows Management Instrumentation],Delete method, IWbemQualifierSet.Delete, IWbemQualifierSet::Delete, _hmm_iwbemqualifierset_delete, wbemcli/IWbemQualifierSet::Delete, wmi.iwbemqualifierset_delete
ms.topic: method
f1_keywords: 
 - "wbemcli/IWbemQualifierSet.Delete"
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
 - IWbemQualifierSet.Delete
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWbemQualifierSet::Delete


## -description


The <b>IWbemQualifierSet::Delete</b> method deletes the specified qualifier by name. Due to qualifier propagation rules, a particular qualifier may have been inherited from another object and merely overridden in the current class or instance. In this case, use the 
<b>Delete</b> method to reset the qualifier to the original inherited value.


## -parameters




### -param wszName [in]

Name of the qualifier to delete. The pointer is treated as read-only.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/qualifier-flavors">Qualifier Flavors</a>
 

 

