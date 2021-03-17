---
UID: NF:wbemcli.IWbemClassObject.GetObjectText
title: IWbemClassObject::GetObjectText (wbemcli.h)
description: The IWbemClassObject::GetObjectText method returns a textual rendering of the object in the MOF syntax.
helpviewer_keywords: ["GetObjectText","GetObjectText method [Windows Management Instrumentation]","GetObjectText method [Windows Management Instrumentation]","IWbemClassObject interface","IWbemClassObject interface [Windows Management Instrumentation]","GetObjectText method","IWbemClassObject.GetObjectText","IWbemClassObject::GetObjectText","_hmm_iwbemclassobject_getobjecttext","wbemcli/IWbemClassObject::GetObjectText","wmi.iwbemclassobject_getobjecttext"]
old-location: wmi\iwbemclassobject_getobjecttext.htm
tech.root: wmi
ms.assetid: 7e874e9a-7417-4b3f-95c5-398fe92bfdf8
ms.date: 12/05/2018
ms.keywords: GetObjectText, GetObjectText method [Windows Management Instrumentation], GetObjectText method [Windows Management Instrumentation],IWbemClassObject interface, IWbemClassObject interface [Windows Management Instrumentation],GetObjectText method, IWbemClassObject.GetObjectText, IWbemClassObject::GetObjectText, _hmm_iwbemclassobject_getobjecttext, wbemcli/IWbemClassObject::GetObjectText, wmi.iwbemclassobject_getobjecttext
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemClassObject::GetObjectText
 - wbemcli/IWbemClassObject::GetObjectText
dev_langs:
 - c++
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
 - IWbemClassObject.GetObjectText
---

# IWbemClassObject::GetObjectText


## -description

The 
<b>IWbemClassObject::GetObjectText</b> method returns a textual rendering of the object in the MOF syntax. Notice that the MOF text returned does not contain all the information about the object, but only enough information for the MOF compiler to be able to re-create the original object. For instance, no propagated qualifiers or parent class properties are displayed.

## -parameters

### -param lFlags [in]

Normally 0. If <b>WBEM_FLAG_NO_FLAVORS</b> is specified, qualifiers will be presented without propagation or flavor information.

### -param pstrObjectText [out]

This must point to <b>NULL</b> on entry. This parameter receives from Windows Management a newly allocated <b>BSTR</b> that was initialized with <b>SysAllocString</b>. You must call <b>SysFreeString</b> on the pointer when the string is no longer required. This pointer points to a MOF syntax rendering of the object upon return from the call. Because this is an out parameter, the pointer must not point to a string that is valid before this method is called, because the pointer will not be deallocated.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

The following algorithm is used to reconstruct the text of the parameters of a method:

<ol>
<li>Parameters are resequenced in the order of their identifier values.</li>
<li>Parameters that are specified as [in] and [out] will be combined into a single parameter.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset">IWbemQualifierSet</a>



<a href="/windows/win32/api/wbemcli/ne-wbemcli-wbem_text_flag_type">WBEM_TEXT_FLAG_TYPE</a>