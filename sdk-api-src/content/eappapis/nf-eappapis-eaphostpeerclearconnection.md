---
UID: NF:eappapis.EapHostPeerClearConnection
title: EapHostPeerClearConnection function
author: windows-driver-content
description: Clears the authentication session connection.
old-location: eaphost\eaphostpeerclearconnection.htm
old-project: EAPHost
ms.assetid: 1d997e4e-6e7f-47db-9957-9658e54c0bdf
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: EapHostPeerClearConnection, EapHostPeerClearConnection function [EAPHost], eaphost.eaphostpeerclearconnection, eappapis/EapHostPeerClearConnection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: eappapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: EapPacket
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	eappprxy.dll
api_name:
-	EapHostPeerClearConnection
product: Windows
targetos: Windows
req.lib: Eappprxy.lib
req.dll: Eappprxy.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EapHostPeerClearConnection function


## -description


Clears the authentication session connection.  After <b>EapHostPeerClearConnection</b> is called, all states associated with <i>pConnectionId</i> are deleted, and no re-authentication associated with this GUID will be initiated. In addition, all future callbacks to the <a href="https://msdn.microsoft.com/7fa12cb4-694a-4db6-9743-5a2cbb995721">NotificationHandler</a> callback function (which was passed by the calling supplicant in  a previous call to  <a href="https://msdn.microsoft.com/9dc339bc-ef01-4432-83cb-b4b14a36f18e">EapHostPeerBeginSession</a>) are halted. 


## -parameters




### -param pConnectionId [in]

 A pointer to a GUID value that uniquely identifies a logical network interface for a connection to terminate between the supplicant and the EAPHost. This connection ID must have been provided in a previous call to <a href="https://msdn.microsoft.com/9dc339bc-ef01-4432-83cb-b4b14a36f18e">EapHostPeerBeginSession</a>.


### -param ppEapError [out]

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure. The address should be set to <b>NULL</b> before calling this function. If error data is available, a pointer to the address of an <b>EAP_ERROR</b> structure that contains any errors raised during the execution of this function call is received. After using the error data, free this memory by calling <a href="https://msdn.microsoft.com/36f9b5dd-821d-4cc5-a1dd-587098635d17">EapHostPeerFreeEapError</a>.


## -see-also




<a href="https://msdn.microsoft.com/b1c473ba-9a12-4929-b4d0-27262117e9c0">EAPHost Supplicant Run-time Functions</a>



<a href="https://msdn.microsoft.com/9dc339bc-ef01-4432-83cb-b4b14a36f18e">EapHostPeerBeginSession</a>



<a href="https://msdn.microsoft.com/6571b50b-f613-4da6-8262-1df2cf97a735">EapHostPeerEndSession</a>
 

 

