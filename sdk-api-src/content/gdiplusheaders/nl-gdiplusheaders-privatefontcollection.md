---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# PrivateFontCollection class


## -description


The <b>PrivateFontCollection</b> is a collection class for fonts. This class keeps a collection of fonts specifically for an application. The fonts in the collection can include installed fonts as well as fonts that have not been installed on the system.


## -remarks



<b>PrivateFontCollection</b> allows applications to install a private version of an existing font without the need to replace the system version of the font. For example, GDI+ can create a private version of the Arial font in addition to the Arial font that the system uses. <b>PrivateFontCollection</b> can also be used to install fonts that don't exist in the operating system. This is a temporary font install that doesn't affect the system-installed collection. To see the installed collection use the 
				<a href="https://msdn.microsoft.com/6c71a3eb-4fbf-45b0-ab35-8756a100af31">InstalledFontCollection</a> class.

<div class="alert"><b>Note</b>  When you use the GDI+ API, you must never allow your application to download arbitrary fonts from untrusted sources. 
The operating system requires elevated privileges to assure that all installed fonts are trusted.</div>
<div> </div>


