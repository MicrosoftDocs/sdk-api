---
UID: NF:gpmgmt.IGPMSOM.GetInheritedGPOLinks
title: IGPMSOM::GetInheritedGPOLinks
author: windows-driver-content
description: Returns a GPOLinksCollection object that contains the GPO links that are applied to the scope of management (SOM), including links inherited from parent containers (OUs and domains).
old-location: gpmc\igpmsom_getinheritedgpolinks.htm
old-project: GPMC
ms.assetid: 545ab05a-b25e-40a7-b002-6935587764a5
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: GPMSOM class [GPMC],GetInheritedGPOLinks method, GetInheritedGPOLinks, GetInheritedGPOLinks method [GPMC], GetInheritedGPOLinks method [GPMC],GPMSOM class, GetInheritedGPOLinks method [GPMC],IGPMSOM interface, IGPMSOM interface [GPMC],GetInheritedGPOLinks method, IGPMSOM.GetInheritedGPOLinks, IGPMSOM::GetInheritedGPOLinks, _win32_igpmsom_getinheritedgpolinks, gpmc.igpmsom_getinheritedgpolinks, gpmgmt/IGPMSOM::GetInheritedGPOLinks
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: GPMStarterGPOType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gpmgmt.dll
api_name:
-	IGPMSOM.GetInheritedGPOLinks
-	GPMSOM.GetInheritedGPOLinks
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMSOM::GetInheritedGPOLinks


## -description


Returns a <a href="https://msdn.microsoft.com/37753a31-0ef8-4fb9-b542-a91ae47ed417">GPOLinksCollection</a> object that contains the GPO links that are applied to the scope of management (SOM), including links inherited from parent containers (OUs and domains). The collection does not include GPO links from site SOMs or disabled links. The collection is sorted in  order of precedence, with the first (earliest) link having the highest priority and last (latest) link having the lowest priority. Note that  the GPOs are applied in  reverse order of their precedence. The last GPO in the list is applied first and the first GPO in the list is applied last.


## -parameters




### -param ppGPOLinks [out]

Address of a pointer to an 
<a href="https://msdn.microsoft.com/37753a31-0ef8-4fb9-b542-a91ae47ed417">IGPMGPOLinksCollection</a> interface.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/37753a31-0ef8-4fb9-b542-a91ae47ed417">GPOLinksCollection</a> object.

<h3>VB</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/37753a31-0ef8-4fb9-b542-a91ae47ed417">GPOLinksCollection</a> object.




## -see-also




<a href="https://msdn.microsoft.com/290a53fb-8be0-477d-837c-46251b30e245">IGPMGPOLink</a>



<a href="https://msdn.microsoft.com/37753a31-0ef8-4fb9-b542-a91ae47ed417">IGPMGPOLinksCollection</a>



<a href="https://msdn.microsoft.com/e3252dba-403d-486d-b666-9bb04ec0aa90">IGPMSOM</a>
 

 

