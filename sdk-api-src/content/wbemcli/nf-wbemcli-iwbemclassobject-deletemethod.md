---
UID: NF:wbemcli.IWbemClassObject.DeleteMethod
title: IWbemClassObject::DeleteMethod (wbemcli.h)
description: Use the IWbemClassObject::DeleteMethod method to delete a method. This call is supported only if the current object is a CIM class definition. Method manipulation is not available from IWbemClassObject pointers which point to CIM instances.
helpviewer_keywords: ["DeleteMethod","DeleteMethod method [Windows Management Instrumentation]","DeleteMethod method [Windows Management Instrumentation]","IWbemClassObject interface","IWbemClassObject interface [Windows Management Instrumentation]","DeleteMethod method","IWbemClassObject.DeleteMethod","IWbemClassObject::DeleteMethod","_hmm_iwbemclassobject_deletemethod","wbemcli/IWbemClassObject::DeleteMethod","wmi.iwbemclassobject_deletemethod"]
old-location: wmi\iwbemclassobject_deletemethod.htm
tech.root: wmi
ms.assetid: 75502b28-1157-4bdd-ba8f-d2cf0c1228c4
ms.date: 12/05/2018
ms.keywords: DeleteMethod, DeleteMethod method [Windows Management Instrumentation], DeleteMethod method [Windows Management Instrumentation],IWbemClassObject interface, IWbemClassObject interface [Windows Management Instrumentation],DeleteMethod method, IWbemClassObject.DeleteMethod, IWbemClassObject::DeleteMethod, _hmm_iwbemclassobject_deletemethod, wbemcli/IWbemClassObject::DeleteMethod, wmi.iwbemclassobject_deletemethod
f1_keywords:
- wbemcli/IWbemClassObject.DeleteMethod
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
- IWbemClassObject.DeleteMethod
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWbemClassObject::DeleteMethod


## -description


Use the 
<b>IWbemClassObject::DeleteMethod</b> method to delete a method. This call is supported only if the current object is a CIM class definition. Method manipulation is not available from 
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> pointers which point to CIM instances.


## -parameters




### -param wszName [in]

Method name to be removed from the class definition.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">System Error Codes</a>.




## -remarks



You may not delete methods inherited from parent classes.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getmethod">IWbemClassObject::GetMethod</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-putmethod">IWbemClassObject::PutMethod</a>
 

 

