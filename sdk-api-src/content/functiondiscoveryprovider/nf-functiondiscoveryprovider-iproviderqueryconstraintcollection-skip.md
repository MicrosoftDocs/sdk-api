---
UID: NF:functiondiscoveryprovider.IProviderQueryConstraintCollection.Skip
title: IProviderQueryConstraintCollection::Skip
author: windows-driver-content
description: Skips the next item in the collection.
old-location: ncd\iproviderqueryconstraintcollection_skip.htm
old-project: FunDisc
ms.assetid: 18c25f6d-387e-46bf-97b6-6bcf195b15e8
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IProviderQueryConstraintCollection interface,Skip method, IProviderQueryConstraintCollection.Skip, IProviderQueryConstraintCollection::Skip, Skip, Skip method, Skip method,IProviderQueryConstraintCollection interface, functiondiscoveryprovider/IProviderQueryConstraintCollection::Skip, ncd.iproviderqueryconstraintcollection_skip
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: functiondiscoveryprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FunctionDiscoveryProvider.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PropertyConstraint
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FunctionDiscoveryProvider.h
api_name:
-	IProviderQueryConstraintCollection.Skip
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# IProviderQueryConstraintCollection::Skip


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Skips the next item in the collection.


## -parameters






## -returns



Possible return values include, but are not limited to, the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
</table>
 




## -remarks



This method works from the beginning of the collection regardless of any get item calls.




## -see-also




<a href="https://msdn.microsoft.com/4d8ff5b9-ec4a-4ec6-b133-3d315f9c017b">IProviderQueryConstraintCollection</a>
 

 

