---
UID: NF:winber.ber_bvfree
title: ber_bvfree function
author: windows-driver-content
description: The ber_bvfree function frees a berval structure.
old-location: ldap\ber_bvfree.htm
old-project: LDAP
ms.assetid: 9e5a4bb9-568d-48ee-be75-952916c021b1
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: "_ldap_ber_bvfree, ber_bvfree, ber_bvfree function [LDAP], ldap.ber__bvfree, ldap.ber_bvfree, winber/ber_bvfree, winldap/ber_bvfree"
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	ber_bvfree
product: Windows
targetos: Windows
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ber_bvfree function


## -description


The <b>ber_bvfree</b> function frees a 
<a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a> structure.


## -parameters




### -param pBerVal [in]

Pointer to the <a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a> structure to be deallocated.


## -returns



None.




## -remarks



Applications should not call this function to free <a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a> structures that they themselves have allocated.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a>
 

 

