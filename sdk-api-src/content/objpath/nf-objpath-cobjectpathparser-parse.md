---
UID: NF:objpath.CObjectPathParser.Parse
title: CObjectPathParser::Parse (objpath.h)
author: windows-sdk-content
description: Parses a string that contains a WMI path into a structure the contains the path parts, such as the server, namespace, class, key that identifies an instance, and others. Use of this object is not recommended. Instead, use the IWbemPath COM interface.
old-location: wmi\cobjectpathparser_parse.htm
tech.root: WmiSdk
ms.assetid: c39dbef5-9050-487a-8e06-17087753330d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "?Parse@CObjectPathParser@@QAEHPBGPAPAUParsedObjectPath@@@Z, ?Parse@CObjectPathParser@@QEAAHPEBGPEAPEAUParsedObjectPath@@@Z, CObjectPathParser interface [Windows Management Instrumentation],Parse method, CObjectPathParser.Parse, CObjectPathParser::Parse, Parse, Parse method [Windows Management Instrumentation], Parse method [Windows Management Instrumentation],CObjectPathParser interface, objpath/CObjectPathParser::Parse, wmi.cobjectpathparser_parse"
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
 - CObjectPathParser.Parse
 - ?Parse@CObjectPathParser@@QAEHPBGPAPAUParsedObjectPath@@@Z
 - ?Parse@CObjectPathParser@@QEAAHPEBGPEAPEAUParsedObjectPath@@@Z
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CObjectPathParser::Parse


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/0138c48f-f61b-4127-adc2-bdf4da06f938">CObjectPathParser</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

Parses a string that contains a WMI path into a structure the contains the path parts, such as the server, namespace, class, key that identifies an instance, and others. Use of  this object is not recommended. Instead, use the <a href="https://msdn.microsoft.com/71b2597b-d82a-439d-b0b7-af76aefea6a2">IWbemPath</a> COM interface.


## -parameters




### -param RawPath [in]

The raw path data.


### -param pOutput [out]

A structure that contains the parsed path parts.


## -see-also




<a href="https://msdn.microsoft.com/0138c48f-f61b-4127-adc2-bdf4da06f938">CObjectPathParser</a>
 

 

