---
UID: NF:uiautomationclient.IUIAutomation2.get_TransactionTimeout
title: IUIAutomation2::get_TransactionTimeout (uiautomationclient.h)
description: Specifies the length of time that UI Automation will wait for a provider to respond to a client request for information about an automation element. (Get)
helpviewer_keywords: ["IUIAutomation2 interface [Windows Accessibility]","TransactionTimeout property","IUIAutomation2.TransactionTimeout","IUIAutomation2.get_TransactionTimeout","IUIAutomation2::TransactionTimeout","IUIAutomation2::get_TransactionTimeout","IUIAutomation2::put_TransactionTimeout","TransactionTimeout property [Windows Accessibility]","TransactionTimeout property [Windows Accessibility]","IUIAutomation2 interface","get_TransactionTimeout","uiautomationclient/IUIAutomation2::TransactionTimeout","uiautomationclient/IUIAutomation2::get_TransactionTimeout","uiautomationclient/IUIAutomation2::put_TransactionTimeout","winauto.uiauto_iuiautomation2_transactiontimeout"]
old-location: winauto\uiauto_iuiautomation2_transactiontimeout.htm
tech.root: WinAuto
ms.assetid: 05E010BA-E35D-45D7-8B2C-0099CE086FE3
ms.date: 12/05/2018
ms.keywords: IUIAutomation2 interface [Windows Accessibility],TransactionTimeout property, IUIAutomation2.TransactionTimeout, IUIAutomation2.get_TransactionTimeout, IUIAutomation2::TransactionTimeout, IUIAutomation2::get_TransactionTimeout, IUIAutomation2::put_TransactionTimeout, TransactionTimeout property [Windows Accessibility], TransactionTimeout property [Windows Accessibility],IUIAutomation2 interface, get_TransactionTimeout, uiautomationclient/IUIAutomation2::TransactionTimeout, uiautomationclient/IUIAutomation2::get_TransactionTimeout, uiautomationclient/IUIAutomation2::put_TransactionTimeout, winauto.uiauto_iuiautomation2_transactiontimeout
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomation2::get_TransactionTimeout
 - uiautomationclient/IUIAutomation2::get_TransactionTimeout
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IUIAutomation2.TransactionTimeout
 - IUIAutomation2.get_TransactionTimeout
 - IUIAutomation2.put_TransactionTimeout
---

# IUIAutomation2::get_TransactionTimeout


## -description

Specifies the length of time that UI Automation will wait for a provider to respond to a client request for information about an automation element. 

This property is read/write.

## -parameters

### -param timeout [out]

Type: <b>DWORD</b>

The duration of the time-out period, in milliseconds.

## -remarks

The default transaction timeout value is 20 seconds.  Because some operations require the provider to process hundreds of elements, the provider might need a significant amount of time to return information to the client.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation2">IUIAutomation2</a>
