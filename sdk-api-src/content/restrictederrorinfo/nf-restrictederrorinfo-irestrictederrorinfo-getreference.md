---
UID: NF:restrictederrorinfo.IRestrictedErrorInfo.GetReference
title: IRestrictedErrorInfo::GetReference method
author: windows-driver-content
description: Returns a reference to restricted error information.
old-location: winrt\irestrictederrorinfo_getreference.htm
old-project: WinRT
ms.assetid: e7f0c451-c6a4-49ec-a97a-dc834081b3c1
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: GetReference method [Windows Runtime], GetReference method [Windows Runtime], IRestrictedErrorInfo interface, GetReference,IRestrictedErrorInfo.GetReference, IRestrictedErrorInfo, IRestrictedErrorInfo interface [Windows Runtime], GetReference method, IRestrictedErrorInfo::GetReference, restrictederrorinfo/IRestrictedErrorInfo::GetReference, winrt.irestrictederrorinfo_getreference
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: restrictederrorinfo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RestrictedErrorInfo.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RM_UNIQUE_PROCESS, *PRM_UNIQUE_PROCESS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	RestrictedErrorInfo.h
api_name:
-	IRestrictedErrorInfo.GetReference
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IRestrictedErrorInfo::GetReference method


## -description


Returns a reference to restricted error information. 


## -parameters




### -param reference [out]

Type: <b>BSTR*</b>

A reference to the error information.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1af8d4bf-1217-44ca-b0dd-9a6feda16100">IRestrictedErrorInfo</a>
 

 

