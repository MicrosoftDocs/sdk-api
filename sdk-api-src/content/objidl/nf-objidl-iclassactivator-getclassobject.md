---
UID: NF:objidl.IClassActivator.GetClassObject
title: IClassActivator::GetClassObject
author: windows-sdk-content
description: Retrieves a class object.
old-location: com\iclassactivator_getclassobject.htm
old-project: com
ms.assetid: 1bbffe63-bd3a-40c8-aece-63121a437269
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetClassObject, GetClassObject method [COM], GetClassObject method [COM],IClassActivator interface, IClassActivator interface [COM],GetClassObject method, IClassActivator.GetClassObject, IClassActivator::GetClassObject, _com_iclassactivator_getclassobject, com.iclassactivator_getclassobject, objidl/IClassActivator::GetClassObject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ObjIdl.h
api_name:
-	IClassActivator.GetClassObject
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IClassActivator::GetClassObject


## -description


Retrieves a class object.


## -parameters




### -param rclsid [in]

The CLSID that identifies the class whose class object is to be retrieved.


### -param dwClassContext [in]

The context in which the class is expected to run. For a list of values, see the <a href="https://msdn.microsoft.com/dcb82ff2-56e4-4c7e-a621-7ffd0f1a9d8e">CLSCTX</a> enumeration.


### -param locale [in]

An LCID constant as defined in WinNls.h.


### -param riid [in]

The IID of the interface on the object to which a pointer is desired.


### -param ppv [out]

The address of pointer variable that receives the interface pointer requested in <i>riid</i>. Upon successful return, *<i>ppv</i> contains the requested interface pointer.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, it is E_FAIL.




## -see-also




<a href="https://msdn.microsoft.com/65e758ce-50a4-49e8-b3b2-0cd148d2781a">CoGetClassObject</a>



<a href="https://msdn.microsoft.com/4f34c5a4-46c0-4391-9c64-cbb6a366e2dc">IClassActivator</a>
 

 

