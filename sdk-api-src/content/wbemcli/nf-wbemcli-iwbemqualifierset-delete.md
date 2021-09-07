---
UID: NF:wbemcli.IWbemQualifierSet.Delete
title: IWbemQualifierSet::Delete (wbemcli.h)
description: The IWbemQualifierSet::Delete method deletes the specified qualifier by name.
helpviewer_keywords: ["Delete","Delete method [Windows Management Instrumentation]","Delete method [Windows Management Instrumentation]","IWbemQualifierSet interface","IWbemQualifierSet interface [Windows Management Instrumentation]","Delete method","IWbemQualifierSet.Delete","IWbemQualifierSet::Delete","_hmm_iwbemqualifierset_delete","wbemcli/IWbemQualifierSet::Delete","wmi.iwbemqualifierset_delete"]
old-location: wmi\iwbemqualifierset_delete.htm
tech.root: wmi
ms.assetid: 77e61fd1-a835-4ed7-8880-9eab65611ebc
ms.date: 12/05/2018
ms.keywords: Delete, Delete method [Windows Management Instrumentation], Delete method [Windows Management Instrumentation],IWbemQualifierSet interface, IWbemQualifierSet interface [Windows Management Instrumentation],Delete method, IWbemQualifierSet.Delete, IWbemQualifierSet::Delete, _hmm_iwbemqualifierset_delete, wbemcli/IWbemQualifierSet::Delete, wmi.iwbemqualifierset_delete
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemQualifierSet::Delete
 - wbemcli/IWbemQualifierSet::Delete
dev_langs:
 - c++
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
---

# IWbemQualifierSet::Delete


## -description

The <b>IWbemQualifierSet::Delete</b> method deletes the specified qualifier by name. Due to qualifier propagation rules, a particular qualifier may have been inherited from another object and merely overridden in the current class or instance. In this case, use the 
<b>Delete</b> method to reset the qualifier to the original inherited value.

## -parameters

### -param wszName [in]

Name of the qualifier to delete. The pointer is treated as read-only.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

## -see-also

<a href="/windows/desktop/WmiSdk/qualifier-flavors">Qualifier Flavors</a>