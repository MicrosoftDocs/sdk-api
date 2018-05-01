---
UID: NF:objpath.CObjectPathParser.Unparse
title: CObjectPathParser::Unparse method
author: windows-driver-content
description: Converts a structure that contains the parsed path to a string. Use of this object is not recommended. Instead, use the IWbemPath COM interface.
old-location: wmi\cobjectpathparser_unparse.htm
old-project: WmiSdk
ms.assetid: 6135b808-b9eb-4ba0-9eb8-e7a59993ae34
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: CObjectPathParser, CObjectPathParser interface [Windows Management Instrumentation], UnParse method, CObjectPathParser::UnParse, CObjectPathParser::Unparse, UnParse method [Windows Management Instrumentation], UnParse method [Windows Management Instrumentation], CObjectPathParser interface, Unparse,CObjectPathParser.Unparse, objpath/CObjectPathParser::UnParse, wmi.cobjectpathparser_unparse
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objpath.h
req.include-header: ObjPath.h
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
req.typenames: ObjectParserFlags
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FrameDynOS.dll
-	FrameDyn.dll
api_name:
-	CObjectPathParser.UnParse
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# CObjectPathParser::Unparse method


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/0138c48f-f61b-4127-adc2-bdf4da06f938">CObjectPathParser</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

Converts a structure that contains the parsed path to a string. Use of  this object is not recommended. Instead, use the <a href="https://msdn.microsoft.com/71b2597b-d82a-439d-b0b7-af76aefea6a2">IWbemPath</a> COM interface.


## -parameters




### -param pInput [in]

A structure that contains WMI path parts such as server, namespaces, classes, key value identifying a specific instance, and others.


### -param pwszPath [out]

A structure that contains the WMI path.


## -remarks



<b>UnParse</b> is a static method.




## -see-also




<a href="https://msdn.microsoft.com/0138c48f-f61b-4127-adc2-bdf4da06f938">CObjectPathParser</a>
 

 

