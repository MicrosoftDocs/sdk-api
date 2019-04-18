---
UID: NF:objbase.CoIsOle1Class
title: CoIsOle1Class function (objbase.h)
author: windows-sdk-content
description: Determines whether the specified CLSID represents an OLE 1 object.
old-location: com\coisole1class.htm
tech.root: com
ms.assetid: 3f6a021d-c8fe-40dd-9c3a-30f22ad76ce3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CoIsOle1Class, CoIsOle1Class function [COM], _com_CoIsOle1Class, com.coisole1class, objbase/CoIsOle1Class
ms.topic: function
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - CoIsOle1Class
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CoIsOle1Class function


## -description


Determines whether the specified CLSID represents an OLE 1 object. 




## -parameters




### -param rclsid [in]

The CLSID to be checked.


## -returns



If the CLSID refers to an OLE 1 object, the return value is <b>TRUE</b>; otherwise, it is <b>FALSE</b>.




## -remarks



The <b>CoIsOle1Class</b> function determines whether an object class is from OLE 1. You can use it to prevent linking to embedded OLE 1 objects within a container, which OLE 1 objects do not support. After a container has determined that copied data represents an embedded object, the container code can call <b>CoIsOle1Class</b> to determine whether the embedded object is an OLE 1 object. If <b>CoIsOle1Class</b> returns <b>TRUE</b>, the container does not offer CF_LINKSOURCE as one of its clipboard formats. This is one of several OLE compatibility functions. The following compatibility functions, listed below, can be used to convert the storage formats of objects between OLE 1 and OLE.


<ul>
<li>
<a href="https://msdn.microsoft.com/d100d32a-6559-4a7c-a0ae-780bc9d82611">OleConvertIStorageToOLESTREAM</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a6026b71-4223-40ab-b209-44531480db57">OleConvertIStorageToOLESTREAMEx</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8fed879c-5f97-4450-8259-da9643dd828c">OleConvertOLESTREAMToIStorage</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2e77fa0e-1d98-4c59-8d3c-65bd7235ec8f">OleConvertOLESTREAMToIStorageEx</a>
</li>
</ul>


