---
UID: NF:wbemdisp.ISWbemObject.GetObjectText_
title: ISWbemObject::GetObjectText_
author: windows-sdk-content
description: The GetObjectText_ method of the SWbemObject object returns a textual rendering of the object.
old-location: wmi\swbemobject_getobjecttext_.htm
old-project: WmiSdk
ms.assetid: 8b980863-14ad-4884-8897-dd076d927824
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: GetObjectText_, GetObjectText_ method [Windows Management Instrumentation], GetObjectText_ method [Windows Management Instrumentation],ISWbemObject interface, GetObjectText_ method [Windows Management Instrumentation],SWbemObject object, ISWbemObject interface [Windows Management Instrumentation],GetObjectText_ method, ISWbemObject.GetObjectText_, ISWbemObject::GetObjectText_, SWbemObject object [Windows Management Instrumentation],GetObjectText_ method, SWbemObject.GetObjectText_, _hmm_swbemobject.getobjecttext_, wmi.swbemobject_getobjecttext_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemdisp.h
req.include-header: 
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
 - SWbemObject.GetObjectText_
 - ISWbemObject.GetObjectText_
 - ISWbemObject.GetObjectText_
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemObject::GetObjectText_


## -description


The 
<b>GetObjectText_</b> method of the 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object returns a textual rendering of the object. This object can be used to display an object's contents. Currently, only the MOF syntax is supported as an output format. Notice that the MOF text returned does not contain all the information about the object; the MOF text contains only enough information for the MOF compiler to be able to re-create the original object. For instance, there is no information about the propagated qualifiers or the parent class properties.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param iFlags [in, optional]

Reserved and must be 0 (zero) if specified.


### -param strObjectText






## -returns



If successful, this method returns a string that contains the output text.



