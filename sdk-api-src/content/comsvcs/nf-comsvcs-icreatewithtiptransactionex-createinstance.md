---
UID: NF:comsvcs.ICreateWithTipTransactionEx.CreateInstance
title: ICreateWithTipTransactionEx::CreateInstance (comsvcs.h)
description: Creates a COM+ object that executes within the scope of the manual transaction specified by a TIP transaction URL.
helpviewer_keywords: ["CreateInstance","CreateInstance method [COM+]","CreateInstance method [COM+]","ICreateWithTipTransactionEx interface","ICreateWithTipTransactionEx interface [COM+]","CreateInstance method","ICreateWithTipTransactionEx.CreateInstance","ICreateWithTipTransactionEx::CreateInstance","_dtc_ICreateWithTipTransactionEx_CreateInstance","comsvcs/ICreateWithTipTransactionEx::CreateInstance","cos.icreatewithtiptransactionex_createinstance"]
old-location: cos\icreatewithtiptransactionex_createinstance.htm
tech.root: cos
ms.assetid: 3f0572eb-8633-4dc3-a013-9cf859241cd7
ms.date: 12/05/2018
ms.keywords: CreateInstance, CreateInstance method [COM+], CreateInstance method [COM+],ICreateWithTipTransactionEx interface, ICreateWithTipTransactionEx interface [COM+],CreateInstance method, ICreateWithTipTransactionEx.CreateInstance, ICreateWithTipTransactionEx::CreateInstance, _dtc_ICreateWithTipTransactionEx_CreateInstance, comsvcs/ICreateWithTipTransactionEx::CreateInstance, cos.icreatewithtiptransactionex_createinstance
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICreateWithTipTransactionEx::CreateInstance
 - comsvcs/ICreateWithTipTransactionEx::CreateInstance
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ICreateWithTipTransactionEx.CreateInstance
---

# ICreateWithTipTransactionEx::CreateInstance


## -description

<p class="CCE_Message">[The TIP service feature are deprecated and might not be available in future versions of the operating system. Consider using the WS-AtomicTransaction (WS-AT) protocol as a replacement transaction coordination and propagation technology. For more information about WS-AT support in the .Net Framework, see <a href="/dotnet/framework/wcf/feature-details/transactions-in-wcf">Transactions</a>.]

Creates a COM+ object that executes within the scope of the manual transaction specified by a TIP transaction URL.

## -parameters

### -param bstrTipUrl [in]

The Transaction Internet Protocol (TIP) URL of the existing transaction in which you want to create the COM+ object.

### -param rclsid [in]

The CLSID of the type of object to be instantiated.

### -param riid [in]

The ID of the interface to be returned by the <i>ppvObj</i> parameter.

### -param pObject [out]

A reference to a new object of the type specified by the <i>rclsid</i> argument, through the interface specified by the <i>riid</i> argument.

## -returns

This method can return the following values:

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icreatewithtiptransactionex">ICreateWithTipTransactionEx</a>