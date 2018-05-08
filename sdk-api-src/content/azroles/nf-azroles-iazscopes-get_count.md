---
UID: NF:azroles.IAzScopes.get_Count
title: IAzScopes::get_Count
author: windows-driver-content
description: Retrieves the number of IAzScope objects in the collection.
old-location: security\iazscopes_count.htm
old-project: SecAuthZ
ms.assetid: aff809a6-c768-4cfe-a41f-ee227f77a3b1
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: AzScopes object [Security],Count property, Count property [Security], Count property [Security],AzScopes object, Count property [Security],IAzScopes interface, IAzScopes interface [Security],Count property, IAzScopes.Count, IAzScopes.get_Count, IAzScopes::Count, IAzScopes::get_Count, azroles/IAzScopes::Count, azroles/IAzScopes::get_Count, get_Count, security.iazscopes_count
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AZ_PROP_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Azroles.dll
api_name:
-	IAzScopes.Count
-	IAzScopes.get_Count
-	AzScopes.Count
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzScopes::get_Count


## -description


The <b>Count</b> property retrieves the number of <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a> objects in the collection.

This property is read-only.


## -parameters


## -remarks



The <b>Count</b> property can be used to specify the last <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a> object in a collection when retrieving a specific <b>IAzScope</b> object using the  <a href="https://msdn.microsoft.com/857fbe67-9b47-4641-9228-fe0e83ef6d4d">IAzScopes.Item</a> property.



