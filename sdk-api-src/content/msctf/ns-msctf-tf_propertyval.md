---
UID: NS:msctf.TF_PROPERTYVAL
title: TF_PROPERTYVAL
author: windows-sdk-content
description: The TF_PROPERTYVAL structure contains property value data. This structure is used with the IEnumTfPropertyValue::Next method.
old-location: tsf\tf_propertyval.htm
old-project: TSF
ms.assetid: 50a5930c-ba17-4441-99a7-efc6c4bfc2ab
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: TF_PROPERTYVAL, TF_PROPERTYVAL structure [Text Services Framework], _tsf_tf_propertyval_ref, msctf/TF_PROPERTYVAL, tsf.tf_propertyval
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TF_PROPERTYVAL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Msctf.h
api_name:
-	TF_PROPERTYVAL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# TF_PROPERTYVAL structure


## -description



The <b>TF_PROPERTYVAL</b> structure contains property value data. This structure is used with the <a href="https://msdn.microsoft.com/b0fe154c-df33-443d-95a2-f41e7b02def8">IEnumTfPropertyValue::Next</a> method.




## -struct-fields




### -field guidId

A <b>GUID</b> that identifies the property type. This can be a custom identifier or one of the <a href="https://msdn.microsoft.com/d88f2eba-4c98-4b32-96e1-cd019fe0f7ad">predefined property identifiers</a>.


### -field varValue

A <b>VARIANT</b> that contains the value of the property specified by <b>guidId</b>. The user must know the type and format of this data.


## -see-also




<a href="https://msdn.microsoft.com/b0fe154c-df33-443d-95a2-f41e7b02def8">IEnumTfPropertyValue::Next
      </a>



<a href="https://msdn.microsoft.com/d88f2eba-4c98-4b32-96e1-cd019fe0f7ad">
        Predefined Properties
      </a>
 

 

