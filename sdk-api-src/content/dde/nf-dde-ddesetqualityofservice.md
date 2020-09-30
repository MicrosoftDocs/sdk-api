---
UID: NF:dde.DdeSetQualityOfService
title: DdeSetQualityOfService function (dde.h)
description: Specifies the quality of service (QOS) a raw Dynamic Data Exchange (DDE) application desires for future DDE conversations it initiates.
helpviewer_keywords: ["DdeSetQualityOfService","DdeSetQualityOfService function [Data Exchange]","_win32_DdeSetQualityOfService","_win32_ddesetqualityofservice_cpp","dataxchg.ddesetqualityofservice","dde/DdeSetQualityOfService","winui._win32_ddesetqualityofservice"]
old-location: dataxchg\ddesetqualityofservice.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchange\dynamicdataexchangereference\dynamicdataexchangefunctions\ddesetqualityofservice.htm
ms.date: 12/05/2018
ms.keywords: DdeSetQualityOfService, DdeSetQualityOfService function [Data Exchange], _win32_DdeSetQualityOfService, _win32_ddesetqualityofservice_cpp, dataxchg.ddesetqualityofservice, dde/DdeSetQualityOfService, winui._win32_ddesetqualityofservice
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DdeSetQualityOfService
 - dde/DdeSetQualityOfService
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - DdeSetQualityOfService
---

# DdeSetQualityOfService function


## -description

Specifies the quality of service (QOS) a raw Dynamic Data Exchange (DDE) application desires for future DDE conversations it initiates. The specified QOS applies to any conversations started while those settings are in place. A DDE conversation's quality of service lasts for the duration of the conversation; calls to the <b>DdeSetQualityOfService</b> function during a conversation do not affect that conversation's QOS.

## -parameters

### -param hwndClient [in]

Type: <b>HWND</b>

A handle to the DDE client window that specifies the source of <a href="/windows/desktop/dataxchg/wm-dde-initiate">WM_DDE_INITIATE</a> messages a client will send to start DDE conversations.

### -param pqosNew [in]

Type: <b>const <a href="/windows/desktop/api/winnt/ns-winnt-security_quality_of_service">SECURITY_QUALITY_OF_SERVICE</a>*</b>

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-security_quality_of_service">SECURITY_QUALITY_OF_SERVICE</a> structure for the desired quality of service values.

### -param pqosPrev [out]

Type: <b>PSECURITY_QUALITY_OF_SERVICE</b>

A pointer to a 
					<a href="/windows/desktop/api/winnt/ns-winnt-security_quality_of_service">SECURITY_QUALITY_OF_SERVICE</a> structure that receives the previous quality of service values associated with the window identified by 
					<i>hwndClient</i>. 

This parameter is optional. If an application has no interest in 
					<i>hwndClient</i>'s previous QOS values, it should set 
					<i>pqosPrev</i> to <b>NULL</b>.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If a quality of service has not been specified for a client window, 
				<i>hwndClient</i>, prior to sending a <a href="/windows/desktop/dataxchg/wm-dde-initiate">WM_DDE_INITIATE</a> with the 
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

<a href="/windows/desktop/dataxchg/about-dynamic-data-exchange">About Dynamic Data Exchange</a>



<b>Conceptual</b>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/api/winnt/ns-winnt-security_quality_of_service">SECURITY_QUALITY_OF_SERVICE</a>



<a href="/windows/desktop/dataxchg/wm-dde-initiate">WM_DDE_INITIATE</a>