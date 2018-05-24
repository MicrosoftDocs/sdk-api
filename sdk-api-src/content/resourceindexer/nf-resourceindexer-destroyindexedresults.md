---
UID: NF:resourceindexer.DestroyIndexedResults
title: DestroyIndexedResults function
author: windows-driver-content
description: Frees the parameters that the IndexFilePath method returned.
old-location: menurc\destroyindexedresults.htm
old-project: menurc
ms.assetid: 0E1D8CC6-B662-4068-A6BA-822E79321C33
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: DestroyIndexedResults, DestroyIndexedResults function [Menus and Other Resources], menurc.destroyindexedresults, resourceindexer/DestroyIndexedResults
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: resourceindexer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WitnessTagUpdateHelper
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mrmsupport.dll
api_name:
-	DestroyIndexedResults
product: Windows
targetos: Windows
req.lib: Mrmsupport.lib
req.dll: Mrmsupport.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# DestroyIndexedResults function


## -description


Frees the parameters that the <a href="https://msdn.microsoft.com/A1CDA9D1-9FEE-4FCB-AA85-1DA58D9EF95B">IndexFilePath</a> method returned.


## -parameters




### -param resourceUri [in, optional]

A uniform resource indicator (URI) that uses the ms-resource URI scheme and represents the named resource for the candidate, where the authority of the URI or the resource map is empty. For example, ms-resource:///Resources/String1 or ms-resource:///Files/images/logo.png.


### -param qualifierCount [in]

The number of indexed resource qualifiers that the list in the <i>ppQualifiers</i> parameter contains.


### -param qualifiers [in, optional]

A list of indexed resource qualifiers that declare the context under which the resources are appropriate.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/A1CDA9D1-9FEE-4FCB-AA85-1DA58D9EF95B">IndexFilePath</a>



<a href="https://msdn.microsoft.com/A6F253AD-0756-4996-AC6C-5B09C55DE22E">IndexedResourceQualifier</a>
 

 

