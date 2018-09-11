---
UID: NF:dde.DdeSetQualityOfService
title: DdeSetQualityOfService function
author: windows-sdk-content
description: Specifies the quality of service (QOS) a raw Dynamic Data Exchange (DDE) application desires for future DDE conversations it initiates.
old-location: dataxchg\ddesetqualityofservice.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchange\dynamicdataexchangereference\dynamicdataexchangefunctions\ddesetqualityofservice.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DdeSetQualityOfService, DdeSetQualityOfService function [Data Exchange], _win32_DdeSetQualityOfService, _win32_ddesetqualityofservice_cpp, dataxchg.ddesetqualityofservice, dde/DdeSetQualityOfService, winui._win32_ddesetqualityofservice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dde.h
req.include-header: Windows.h
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - DdeSetQualityOfService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DdeSetQualityOfService function


## -description


Specifies the quality of service (QOS) a raw Dynamic Data Exchange (DDE) application desires for future DDE conversations it initiates. The specified QOS applies to any conversations started while those settings are in place. A DDE conversation's quality of service lasts for the duration of the conversation; calls to the <b>DdeSetQualityOfService</b> function during a conversation do not affect that conversation's QOS. 


## -parameters




### -param hwndClient [in]

Type: <b>HWND</b>

A handle to the DDE client window that specifies the source of <a href="https://msdn.microsoft.com/en-us/library/ms648996(v=VS.85).aspx">WM_DDE_INITIATE</a> messages a client will send to start DDE conversations. 


### -param pqosNew [in]

Type: <b>const <a href="https://msdn.microsoft.com/21f99d04-b21b-442c-9034-35f9f7bbee53">SECURITY_QUALITY_OF_SERVICE</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/21f99d04-b21b-442c-9034-35f9f7bbee53">SECURITY_QUALITY_OF_SERVICE</a> structure for the desired quality of service values. 


### -param pqosPrev [out]

Type: <b>PSECURITY_QUALITY_OF_SERVICE</b>

A pointer to a 
					<a href="https://msdn.microsoft.com/21f99d04-b21b-442c-9034-35f9f7bbee53">SECURITY_QUALITY_OF_SERVICE</a> structure that receives the previous quality of service values associated with the window identified by 
					<i>hwndClient</i>. 

This parameter is optional. If an application has no interest in 
					<i>hwndClient</i>'s previous QOS values, it should set 
					<i>pqosPrev</i> to <b>NULL</b>.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



If a quality of service has not been specified for a client window, 
				<i>hwndClient</i>, prior to sending a <a href="https://msdn.microsoft.com/en-us/library/ms648996(v=VS.85).aspx">WM_DDE_INITIATE</a> with the 
				<i>wParam</i> set to 
				<i>hwndClient</i>, the system uses the following default quality of service values for the client window: 


```
{ 
   Length = sizeof(SECURITY_QUALITY_OF_SERVICE); 
   ImpersonationLevel = SecurityImpersonation; 
   ContextTrackingMode = SECURITY_STATIC_TRACKING; 
   EffectiveOnly = TRUE; 
} 
```


Use the <b>DdeSetQualityOfService</b> function to associate a different quality of service with the client window. After you change the quality of service, the new settings affect any subsequent conversations that are started. Once an application starts a DDE conversation using a particular quality of service value, it must terminate the conversation and restart the conversation in order to have a different value take effect. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms648774(v=VS.85).aspx">About Dynamic Data Exchange</a>



<b>Conceptual</b>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/21f99d04-b21b-442c-9034-35f9f7bbee53">SECURITY_QUALITY_OF_SERVICE</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648996(v=VS.85).aspx">WM_DDE_INITIATE</a>
 

 

