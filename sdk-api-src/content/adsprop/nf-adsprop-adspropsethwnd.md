---
UID: NF:adsprop.ADsPropSetHwnd
title: ADsPropSetHwnd function
author: windows-sdk-content
description: Used to notify the notification object of the property page window handle.
old-location: ad\adspropsethwnd.htm
old-project: AD
ms.assetid: 9fc6b86b-e075-4969-842c-3ebddd43db8f
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: ADsPropSetHwnd, ADsPropSetHwnd function [Active Directory], _glines_adspropsethwnd, ad.adspropsethwnd, adsprop/ADsPropSetHwnd
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: adsprop.h
req.include-header: 
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
tech.root: 
req.typenames: DOT11_ADHOC_NETWORK_CONNECTION_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dsprop.dll
api_name:
 - ADsPropSetHwnd
product: Windows
targetos: Windows
req.lib: Dsprop.lib
req.dll: Dsprop.dll
req.irql: 
---

# ADsPropSetHwnd function


## -description


The <b>ADsPropSetHwnd</b> function is used to notify the notification object of the property page window handle.


## -parameters




### -param hNotifyObj

TBD


### -param hPage [in]

A window handle of the property page.


#### - hNotifyObject [in]

The handle of the notification object. To obtain this handle, call <a href="https://msdn.microsoft.com/bfca3801-0d24-4177-8173-b6bf4b854fae">ADsPropCreateNotifyObj</a>.


## -returns



Returns zero if the notification object does not exist or nonzero otherwise.




## -remarks



An Active Directory Domain Services property sheet extension normally calls this function while processing the <a href="_win32_wm_initdialog_cpp">WM_INITDIALOG</a> message.

If the property sheet extension uses the <a href="https://msdn.microsoft.com/c7ed3d36-474e-4cb1-82aa-1e2c1ebd4b83">ADsPropShowErrorDialog</a> function, the extension should use <a href="https://msdn.microsoft.com/d0d26f32-1c15-4641-bdeb-0f464a510669">ADsPropSetHwndWithTitle</a> rather than <b>ADsPropSetHwnd</b>.




## -see-also




<a href="https://msdn.microsoft.com/bfca3801-0d24-4177-8173-b6bf4b854fae">ADsPropCreateNotifyObj</a>



<a href="https://msdn.microsoft.com/d0d26f32-1c15-4641-bdeb-0f464a510669">ADsPropSetHwndWithTitle</a>



<a href="https://msdn.microsoft.com/c7ed3d36-474e-4cb1-82aa-1e2c1ebd4b83">ADsPropShowErrorDialog</a>



<a href="_win32_wm_initdialog_cpp">WM_INITDIALOG</a>
 

 

