---
UID: NF:winber.ber_init
title: ber_init function
author: windows-sdk-content
description: The ber_init function allocates a new BerElement structure containing the data taken from the supplied berval structure.
old-location: ldap\ber_init.htm
old-project: LDAP
ms.assetid: ad6557e9-1683-4ffd-a59e-8f37eb67d089
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: "_ldap_ber_init, ber_init, ber_init function [LDAP], ldap.ber__init, ldap.ber_init, winber/ber_init"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winber.h
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
req.typenames: WIN32_STREAM_ID, *LPWIN32_STREAM_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wldap32.dll
api_name:
-	ber_init
product: Windows
targetos: Windows
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ber_init function


## -description


The <b>ber_init</b> function allocates a new 
<a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a> structure containing the data taken from the supplied 
<a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a> structure.


## -parameters




### -param pBerVal [in]

Pointer to the source <a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a> structure.


## -returns



If the function succeeds, the return value is a pointer to the newly allocated <a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a> structure.

If the function fails, it returns a <b>NULL</b> pointer.




## -remarks



Call 
<a href="https://msdn.microsoft.com/b0f5a81e-a1d1-41c3-802c-b17be2275964">ber_free</a> to free a <a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a> structure allocated with this function.




## -see-also




<a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/b0f5a81e-a1d1-41c3-802c-b17be2275964">ber_free</a>



<a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a>
 

 

