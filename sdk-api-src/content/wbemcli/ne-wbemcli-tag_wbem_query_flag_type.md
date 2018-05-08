---
UID: NE:wbemcli.tag_WBEM_QUERY_FLAG_TYPE
title: tag_WBEM_QUERY_FLAG_TYPE
author: windows-driver-content
description: Contains flags used to define a query or enumerator.
old-location: wmi\wbem_query_flag_type.htm
old-project: WmiSdk
ms.assetid: D0F53F94-682A-432D-8FBA-8EC05C6B69BF
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: WBEM_FLAG_DEEP, WBEM_FLAG_PROTOTYPE, WBEM_FLAG_SHALLOW, WBEM_QUERY_FLAG_TYPE, WBEM_QUERY_FLAG_TYPE enumeration [Windows Management Instrumentation], tag_WBEM_QUERY_FLAG_TYPE, wbemcli/WBEM_FLAG_DEEP, wbemcli/WBEM_FLAG_PROTOTYPE, wbemcli/WBEM_FLAG_SHALLOW, wbemcli/WBEM_QUERY_FLAG_TYPE, wmi.wbem_query_flag_type
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wbemcli.h
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
req.typenames: WBEM_QUERY_FLAG_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wbemcli.h
api_name:
-	WBEM_QUERY_FLAG_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tag_WBEM_QUERY_FLAG_TYPE enumeration


## -description


Contains flags used to define a query or  enumerator.


## -enum-fields




### -field WBEM_FLAG_DEEP

Include the specified class and all subclasses.


### -field WBEM_FLAG_SHALLOW

Include only the specified class, not any subclasses.


### -field WBEM_FLAG_PROTOTYPE

Used for prototyping. It does not execute the query and instead returns an object that looks like a typical result object.


## -see-also




<a href="https://msdn.microsoft.com/23122b38-5671-4454-be79-85c6bc34daa0">IWbemServices::CreateClassEnum</a>



<a href="https://msdn.microsoft.com/02b81f48-c6a0-44db-86b9-936331b15cc4">IWbemServices::CreateClassEnumAsync</a>



<a href="https://msdn.microsoft.com/47671b9b-a2ff-4375-b2a4-7e8599f1fb69">IWbemServices::CreateInstanceEnum</a>



<a href="https://msdn.microsoft.com/5ba2ff28-034f-4949-9bde-8c98345ec7c6">IWbemServices::CreateInstanceEnumAsync</a>



<a href="https://msdn.microsoft.com/8cb4a42b-f8ae-4a6f-884c-fa808b11dc8a">IWbemServices::ExecQuery</a>



<a href="https://msdn.microsoft.com/d8b55500-d84c-431b-93c6-99d1f1b845c3">IWbemServices::ExecQueryAsync</a>
 

 

