---
UID: NF:wbemcli.IWbemObjectAccess.WritePropertyValue
title: IWbemObjectAccess::WritePropertyValue
author: windows-sdk-content
description: The WritePropertyValue method writes a specified number of bytes to a property identified by a property handle. Use this method to set string and all other non-DWORD or non-QWORD data.
old-location: wmi\iwbemobjectaccess_writepropertyvalue.htm
old-project: WmiSdk
ms.assetid: 2ac2b8b0-8b69-4f01-8017-ace82a382f40
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: IWbemObjectAccess interface [Windows Management Instrumentation],WritePropertyValue method, IWbemObjectAccess.WritePropertyValue, IWbemObjectAccess::WritePropertyValue, WritePropertyValue, WritePropertyValue method [Windows Management Instrumentation], WritePropertyValue method [Windows Management Instrumentation],IWbemObjectAccess interface, _hmm_iwbemobjectaccess_writepropertyvalue, wbemcli/IWbemObjectAccess::WritePropertyValue, wmi.iwbemobjectaccess_writepropertyvalue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemcli.h
req.include-header: Wbemidl.h
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
req.typenames: WMI_OBJ_TEXT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Esscli.dll
 - Fastprox.dll
 - Wbemess.dll
api_name:
 - IWbemObjectAccess.WritePropertyValue
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Esscli.dll; Fastprox.dll; Wbemess.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemObjectAccess::WritePropertyValue


## -description


The <b>WritePropertyValue</b> method writes a specified number of bytes to a property identified by a property handle. Use this method to set string and all other non-<b>DWORD</b> or non-<b>QWORD</b> data.


## -parameters




### -param lHandle [in]

Integer that contains the handle that identifies this property.


### -param lNumBytes [in]

Integer that contains the number of bytes being written to the property. For nonstring property values, <i>lNumBytes</i> must be the correct data size of the property type specified. For string property values such as reference, string, and datetime, <i>lNumBytes</i> must be the length of the specified string in bytes, and the string itself must be of an even length in bytes and be followed with a null-termination character.


### -param aData [in]

Pointer to the constant byte type array that contains the data.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>.




## -see-also




<a href="https://msdn.microsoft.com/1025ae50-870f-4d38-8e83-3c6b628315c6">IWbemObjectAccess</a>
 

 

