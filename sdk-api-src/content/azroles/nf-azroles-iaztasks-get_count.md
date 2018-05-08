---
UID: NF:azroles.IAzTasks.get_Count
title: IAzTasks::get_Count
author: windows-driver-content
description: Retrieves the number of IAzTask objects in the collection.
old-location: security\iaztasks_count.htm
old-project: SecAuthZ
ms.assetid: 505768ce-27a3-4f36-aeea-081cf8e45d14
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: AzTasks object [Security],Count property, Count property [Security], Count property [Security],AzTasks object, Count property [Security],IAzTasks interface, IAzTasks interface [Security],Count property, IAzTasks.Count, IAzTasks.get_Count, IAzTasks::Count, IAzTasks::get_Count, azroles/IAzTasks::Count, azroles/IAzTasks::get_Count, get_Count, security.iaztasks_count
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
-	IAzTasks.Count
-	IAzTasks.get_Count
-	AzTasks.Count
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzTasks::get_Count


## -description


The <b>Count</b> property retrieves the number of <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> objects in the collection.

This property is read-only.


## -parameters


## -remarks



The <b>Count</b> property can be used to specify the last <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object in a collection when retrieving a specific <b>IAzTask</b> object using the  <a href="https://msdn.microsoft.com/eddfebba-4f0e-405a-90b5-dbdc87dca3da">IAzTasks.Item</a> property.



