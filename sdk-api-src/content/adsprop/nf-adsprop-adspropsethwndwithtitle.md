---
UID: NF:adsprop.ADsPropSetHwndWithTitle
title: ADsPropSetHwndWithTitle function
author: windows-driver-content
description: Used to notify the notification object of the property page window handle.
old-location: ad\adspropsethwndwithtitle.htm
old-project: AD
ms.assetid: d0d26f32-1c15-4641-bdeb-0f464a510669
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: ADsPropSetHwndWithTitle, ADsPropSetHwndWithTitle function [Active Directory], ad.adspropsethwndwithtitle, adsprop/ADsPropSetHwndWithTitle
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DOT11_ADHOC_NETWORK_CONNECTION_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dsprop.dll
api_name:
-	ADsPropSetHwndWithTitle
product: Windows
targetos: Windows
req.lib: Dsprop.lib
req.dll: Dsprop.dll
req.irql: 
---

# ADsPropSetHwndWithTitle function


## -description


The <b>ADsPropSetHwndWithTitle</b> function is used to notify the notification object of the property page window handle.
  This function includes the title of the property page which enables the error dialog displayed by <a href="https://msdn.microsoft.com/c7ed3d36-474e-4cb1-82aa-1e2c1ebd4b83">ADsPropShowErrorDialog</a> to provide more useful information to the user.


## -parameters




### -param hNotifyObj

TBD


### -param hPage [in]

A window handle of the property page.


### -param ptzTitle [in]

Pointer to a NULL-terminated string that contains the property page title.


#### - hNotifyObject [in]

The handle of the notification object. To obtain this handle, call <a href="https://msdn.microsoft.com/bfca3801-0d24-4177-8173-b6bf4b854fae">ADsPropCreateNotifyObj</a>.


## -returns



Returns zero if the notification object does not exist or nonzero otherwise.




## -remarks



An Active Directory Domain Services property sheet extension normally calls this function while processing the <a href="_win32_wm_initdialog_cpp">WM_INITDIALOG</a> message.

If the property sheet extension uses the <a href="https://msdn.microsoft.com/c7ed3d36-474e-4cb1-82aa-1e2c1ebd4b83">ADsPropShowErrorDialog</a> function, the extension should use <b>ADsPropSetHwndWithTitle</b> rather than <a href="https://msdn.microsoft.com/9fc6b86b-e075-4969-842c-3ebddd43db8f">ADsPropSetHwnd</a>.




## -see-also




<a href="https://msdn.microsoft.com/bfca3801-0d24-4177-8173-b6bf4b854fae">ADsPropCreateNotifyObj</a>



<a href="https://msdn.microsoft.com/9fc6b86b-e075-4969-842c-3ebddd43db8f">ADsPropSetHwnd</a>



<a href="https://msdn.microsoft.com/c7ed3d36-474e-4cb1-82aa-1e2c1ebd4b83">ADsPropShowErrorDialog</a>



<a href="_win32_wm_initdialog_cpp">WM_INITDIALOG</a>
 

 

