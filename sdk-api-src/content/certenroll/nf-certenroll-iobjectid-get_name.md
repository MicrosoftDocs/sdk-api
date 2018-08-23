---
UID: NF:certenroll.IObjectId.get_Name
title: IObjectId::get_Name
author: windows-sdk-content
description: Retrieves a CERTENROLL_OBJECTID value that contains an object identifier.
old-location: security\iobjectid_name_property.htm
old-project: seccertenroll
ms.assetid: 3d3842a9-73b6-4fb8-83cf-ac65c5a09acb
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IObjectId interface [Security],Name property, IObjectId.Name, IObjectId.get_Name, IObjectId::Name, IObjectId::get_Name, Name property [Security], Name property [Security],IObjectId interface, certenroll/IObjectId::Name, certenroll/IObjectId::get_Name, get_Name, security.iobjectid_name_property
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IObjectId.Name
 - IObjectId.get_Name
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IObjectId::get_Name


## -description


The <b>Name</b> property retrieves a <a href="https://msdn.microsoft.com/en-us/library/Aa374855(v=VS.85).aspx">CERTENROLL_OBJECTID</a> value that contains an <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a>.

This property is read-only.


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
<a href="https://msdn.microsoft.com/en-us/library/Aa376795(v=VS.85).aspx">FriendlyName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376802(v=VS.85).aspx">Value</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa376784(v=VS.85).aspx">IObjectID</a>
 

 

