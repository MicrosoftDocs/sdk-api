---
UID: NF:objpath.CObjectPathParser.Free(ParsedObjectPath)
title: CObjectPathParser::Free(ParsedObjectPath)
author: windows-sdk-content
description: Releases the memory that contains the structure that has the parsed path. Use of this object is not recommended. Instead, use the IWbemPath COM interface.
old-location: wmi\cobjectpathparser_free_parsedobjectpath_.htm
tech.root: WmiSdk
ms.assetid: 7350a0b1-d3e8-48b7-a54d-943bb6709a5b
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: "?Free@CObjectPathParser@@QAEXPAUParsedObjectPath@@@Z, ?Free@CObjectPathParser@@QEAAXPEAUParsedObjectPath@@@Z, CObjectPathParser interface [Windows Management Instrumentation],Free method, CObjectPathParser.Free, CObjectPathParser.Free(ParsedObjectPath), CObjectPathParser::Free, CObjectPathParser::Free(ParsedObjectPath), CObjectPathParser::Free(ParsedObjectPath*), Free, Free method [Windows Management Instrumentation], Free method [Windows Management Instrumentation],CObjectPathParser interface, objpath/CObjectPathParser::Free, wmi.cobjectpathparser_free_parsedobjectpath_"
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
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
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
 - ?Free@CObjectPathParser@@QAEXPAUParsedObjectPath@@@Z
 - ?Free@CObjectPathParser@@QEAAXPEAUParsedObjectPath@@@Z
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CObjectPathParser::Free(ParsedObjectPath)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/0138c48f-f61b-4127-adc2-bdf4da06f938">CObjectPathParser</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

Releases the memory that contains the structure that has the parsed path. Use of  this object is not recommended. Instead, use the <a href="https://msdn.microsoft.com/71b2597b-d82a-439d-b0b7-af76aefea6a2">IWbemPath</a> COM interface.


## -parameters




### -param pOutput [in]

A structure that contains the parsed path.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/0138c48f-f61b-4127-adc2-bdf4da06f938">CObjectPathParser</a>
 

 

