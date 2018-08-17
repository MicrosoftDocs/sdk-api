---
UID: NN:mmcobj.ISnapinPropertiesCallback
title: ISnapinPropertiesCallback
author: windows-sdk-content
description: The ISnapinPropertiesCallback interface adds property names for the snap-in. This interface is implemented by MMC for the snap-in.
old-location: mmc\isnapinpropertiescallback.htm
old-project: mmc
ms.assetid: d02d265c-f3fa-4332-910e-f0d9d4f0687a
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: ISnapinPropertiesCallback, ISnapinPropertiesCallback interface [MMC], ISnapinPropertiesCallback interface [MMC],described, _slate_isnapinpropertiescallback, mmc.isnapinpropertiescallback, mmcobj/ISnapinPropertiesCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mmcobj.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MMC_PROPERTY_ACTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - ISnapinPropertiesCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISnapinPropertiesCallback interface


## -description


The 
<b>ISnapinPropertiesCallback</b> interface adds property names for the snap-in. This interface is implemented by MMC for the snap-in.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISnapinPropertiesCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISnapinPropertiesCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISnapinPropertiesCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44f2536b-c224-4704-b99a-6e7ef21961bc">AddPropertyName</a>
</td>
<td align="left" width="63%">
Adds a property by name for the snap-in to use.

</td>
</tr>
</table> 

