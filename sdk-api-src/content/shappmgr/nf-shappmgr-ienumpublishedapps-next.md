---
UID: NF:shappmgr.IEnumPublishedApps.Next
title: IEnumPublishedApps::Next
author: windows-sdk-content
description: Gets the next IPublishedApp object in the enumeration.
old-location: shell\IEnumPublishedApps_Next.htm
old-project: shell
ms.assetid: 78d18529-2eeb-4510-8703-457ffe998bc5
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IEnumPublishedApps interface [Windows Shell],Next method, IEnumPublishedApps.Next, IEnumPublishedApps::Next, Next, Next method [Windows Shell], Next method [Windows Shell],IEnumPublishedApps interface, inet_IEnumPublishedApps_Next, shappmgr/IEnumPublishedApps::Next, shell.IEnumPublishedApps_Next
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shappmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shappmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PUBAPPINFOFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shappmgr.h
api_name:
 - IEnumPublishedApps.Next
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IEnumPublishedApps::Next


## -description



		Gets the next <a href="https://msdn.microsoft.com/a5a44e74-494a-4c9b-8bf3-85c6093b2c0e">IPublishedApp</a> object in the enumeration.
		


## -parameters




### -param pia






#### - ppApp [out]

Type: <b><a href="https://msdn.microsoft.com/a5a44e74-494a-4c9b-8bf3-85c6093b2c0e">IPublishedApp</a>**</b>


          A pointer to an <a href="https://msdn.microsoft.com/a5a44e74-494a-4c9b-8bf3-85c6093b2c0e">IPublishedApp</a> interface reference variable that returns the next application object. Note that the category of the application object returned must match that passed into <a href="https://msdn.microsoft.com/b24c3007-662a-4c42-9ca7-367180152deb">EnumApps</a>.
        


## -returns



Type: <b>HRESULT</b>


          Returns S_OK if an item is returned, S_FALSE if there are no more items to enumerate, a COM-defined error value otherwise.
        




## -remarks



<div class="alert"><b>Note</b>  <a href="https://msdn.microsoft.com/89a06b1d-1b72-46ca-91cd-bb63ea0cbff7">IEnumPublishedApps</a> is not a standard enumeration interface. It does not support a Skip method, nor does its Next method support retrieval of multiple items.
        </div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/5391444a-53b6-48c9-9a94-d045b3f97182">IAppPublisher</a>



<a href="https://msdn.microsoft.com/89a06b1d-1b72-46ca-91cd-bb63ea0cbff7">IEnumPublishedApps</a>



<a href="https://msdn.microsoft.com/a5a44e74-494a-4c9b-8bf3-85c6093b2c0e">IPublishedApp</a>
 

 

