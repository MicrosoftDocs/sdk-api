---
UID: NF:winldap.ldap_value_freeA
title: ldap_value_freeA function
author: windows-driver-content
description: Frees a structure returned by ldap_get_values.
old-location: ldap\ldap_value_free.htm
old-project: LDAP
ms.assetid: 67c9f04c-4b8e-4e97-902d-fceccf27f522
ms.author: windowsdriverdev
ms.date: 5/15/2018
ms.keywords: "_ldap_ldap_value_free, ldap.ldap__value__free, ldap.ldap_value_free, ldap_value_free, ldap_value_free function [LDAP], ldap_value_freeA, ldap_value_freeW, winldap/ldap_value_free, winldap/ldap_value_freeA, winldap/ldap_value_freeW"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_value_freeW (Unicode) and ldap_value_freeA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VOLUME_GET_GPT_ATTRIBUTES_INFORMATION, *PVOLUME_GET_GPT_ATTRIBUTES_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wldap32.dll
api_name:
-	ldap_value_free
-	ldap_value_freeA
-	ldap_value_freeW
product: Windows
targetos: Windows
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ldap_value_freeA function


## -description


The <b>ldap_value_free</b> function frees a structure returned by 
<a href="https://msdn.microsoft.com/a633afa1-4a37-4894-ae94-5225d99077fd">ldap_get_values</a>.


## -parameters




### -param vals

The structure to free.


## -returns



If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. For more information, see <a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>.




## -remarks



Call <b>ldap_value_free</b> to free a structure returned by <a href="https://msdn.microsoft.com/a633afa1-4a37-4894-ae94-5225d99077fd">ldap_get_values</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/38482501-faa1-4055-9758-e1e0a4199688">Searching a Directory</a>



<a href="https://msdn.microsoft.com/a633afa1-4a37-4894-ae94-5225d99077fd">ldap_get_values</a>
 

 

