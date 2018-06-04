---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ICreateWithTipTransactionEx::CreateInstance


## -description


<p class="CCE_Message">[The TIP service feature are deprecated and might not be available in future versions of the operating system. Consider using the WS-AtomicTransaction (WS-AT) protocol as a replacement transaction coordination and propagation technology. For more information about WS-AT support in the .Net Framework, see <a href="http://go.microsoft.com/fwlink/p/?linkid=105715">Transactions</a>.]

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




<a href="https://msdn.microsoft.com/09927c61-ce64-4d8a-a5b3-542748bfd256">ICreateWithTipTransactionEx</a>
 

 

