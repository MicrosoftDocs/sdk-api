---
UID: NF:certenroll.IObjectId.get_FriendlyName
title: IObjectId::get_FriendlyName
author: windows-sdk-content
description: Specifies and retrieves a display name for the object identifier.
old-location: security\iobjectid_friendlyname_property.htm
tech.root: seccertenroll
ms.assetid: 9360f652-afeb-4f30-a423-402f397b9255
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: FriendlyName property [Security], FriendlyName property [Security],IObjectId interface, IObjectId interface [Security],FriendlyName property, IObjectId.FriendlyName, IObjectId.get_FriendlyName, IObjectId::FriendlyName, IObjectId::get_FriendlyName, IObjectId::put_FriendlyName, certenroll/IObjectId::FriendlyName, certenroll/IObjectId::get_FriendlyName, certenroll/IObjectId::put_FriendlyName, get_FriendlyName, security.iobjectid_friendlyname_property
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IObjectId.FriendlyName
 - IObjectId.get_FriendlyName
 - IObjectId.put_FriendlyName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IObjectId::get_FriendlyName


## -description


The <b>FriendlyName</b> property specifies and retrieves a display name for the object identifier. The display name exists until another name is specified or the object lifetime has ended. This property is web enabled for output.

This property is read/write.


## -parameters


## -remarks



You must call any of the following methods before you can retrieve this property value:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376796(v=VS.85).aspx">InitializeFromAlgorithmName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376797(v=VS.85).aspx">InitializeFromName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376798(v=VS.85).aspx">InitializeFromValue</a>
</li>
</ul>


You can also retrieve the following property values:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376800(v=VS.85).aspx">Name</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376802(v=VS.85).aspx">Value</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa376784(v=VS.85).aspx">IObjectId</a>
 

 

