---
UID: NF:objpath.CObjectPathParser.Free(LPWSTR)
title: CObjectPathParser::Free(LPWSTR)
author: windows-sdk-content
description: Releases the memory that contains the unparsed path. Use of this object is not recommended. Instead, use the IWbemPath COM interface.
old-location: wmi\cobjectpathparser_free_lpwstr_.htm
old-project: WmiSdk
ms.assetid: 3a18a29a-269a-490c-8ede-6ec6b77f99f7
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: CObjectPathParser interface [Windows Management Instrumentation],Free method, CObjectPathParser.Free, CObjectPathParser.Free(LPWSTR), CObjectPathParser::Free, CObjectPathParser::Free(LPWSTR), Free, Free method [Windows Management Instrumentation], Free method [Windows Management Instrumentation],CObjectPathParser interface, objpath/CObjectPathParser::Free, wmi.cobjectpathparser_free_lpwstr_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objpath.h
req.include-header: ObjPath.h
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
req.typenames: ObjectParserFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CObjectPathParser.Free
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: ADAM
---

# CObjectPathParser::Free(LPWSTR)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/0138c48f-f61b-4127-adc2-bdf4da06f938">CObjectPathParser</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

Releases the memory that contains the unparsed path.  Use of  this object is not recommended. Instead, use the <a href="https://msdn.microsoft.com/71b2597b-d82a-439d-b0b7-af76aefea6a2">IWbemPath</a> COM interface.


## -parameters




### -param wszUnparsedPath [in]

Memory containing the unparsed path information.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/0138c48f-f61b-4127-adc2-bdf4da06f938">CObjectPathParser</a>
 

 

