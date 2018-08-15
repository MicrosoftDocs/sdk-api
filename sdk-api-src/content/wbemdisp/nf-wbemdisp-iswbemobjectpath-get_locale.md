---
UID: NF:wbemdisp.ISWbemObjectPath.get_Locale
title: ISWbemObjectPath::get_Locale
author: windows-sdk-content
description: The Locale property of the SWbemObjectPath object contains the locale of object path.
old-location: wmi\swbemobjectpath_locale.htm
old-project: WmiSdk
ms.assetid: cde4ebac-b112-48b5-a274-802e6d3fbfbf
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: ISWbemObjectPath interface [Windows Management Instrumentation],Locale property, ISWbemObjectPath.get_Locale, ISWbemObjectPath.put_Locale, ISWbemObjectPath::get_Locale, Locale property [Windows Management Instrumentation], Locale property [Windows Management Instrumentation],ISWbemObjectPath interface, Locale property [Windows Management Instrumentation],SWbemObjectPath object, SWbemObjectPath object [Windows Management Instrumentation],Locale property, SWbemObjectPath.Locale, _hmm_swbemobjectpath.locale, get_Locale, wmi.swbemobjectpath_locale
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemdisp.h
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
req.type-library: Wbemdisp.tlb
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemdisp.dll
api_name:
 - SWbemObjectPath.Locale
 - ISWbemObjectPath.Locale
 - ISWbemObjectPath.get_Locale
 - ISWbemObjectPath.put_Locale
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemObjectPath::get_Locale


## -description


The 
<b>Locale</b> property of the 
<a href="https://msdn.microsoft.com/f2cf489d-d2a9-4926-84cf-fb33fe3d726a">SWbemObjectPath</a> object contains the locale of object path.

When the <b>SWbemObjectPath.Locale</b> property is part of a standalone 
<a href="https://msdn.microsoft.com/f2cf489d-d2a9-4926-84cf-fb33fe3d726a">SWbemObjectPath</a> object, it is read/write and can be used to set the locale component of the moniker.

When the <b>SWbemObjectPath.Locale</b> property is accessed as part of a 
<a href="https://msdn.microsoft.com/85a55159-5f10-49b5-bc37-39d7b4dfccd7">SWbemObject.Path_</a> property, it is read-only and reports the value of the locale used in binding to the namespace from which the object was obtained.

For Microsoft locale identifiers, the format of the string is "MS_xxxx", where xxxx is a string in hexadecimal form that indicates the LCID. For example, the American English locale identifier is "MS_409".

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.

This property is read/write.


## -parameters

