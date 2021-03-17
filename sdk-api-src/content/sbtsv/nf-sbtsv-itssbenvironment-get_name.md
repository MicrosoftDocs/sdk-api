---
UID: NF:sbtsv.ITsSbEnvironment.get_Name
title: ITsSbEnvironment::get_Name (sbtsv.h)
description: Retrieves a value that indicates the name of the environment that hosts the target computer.
helpviewer_keywords: ["ITsSbEnvironment interface [Remote Desktop Services]","Name property","ITsSbEnvironment.Name","ITsSbEnvironment.get_Name","ITsSbEnvironment::Name","ITsSbEnvironment::get_Name","Name property [Remote Desktop Services]","Name property [Remote Desktop Services]","ITsSbEnvironment interface","get_Name","sbtsv/ITsSbEnvironment::Name","sbtsv/ITsSbEnvironment::get_Name","termserv.itssbenvironment_name"]
old-location: termserv\itssbenvironment_name.htm
tech.root: TermServ
ms.assetid: 8104bdae-f445-425b-b326-cc3333839d29
ms.date: 12/05/2018
ms.keywords: ITsSbEnvironment interface [Remote Desktop Services],Name property, ITsSbEnvironment.Name, ITsSbEnvironment.get_Name, ITsSbEnvironment::Name, ITsSbEnvironment::get_Name, Name property [Remote Desktop Services], Name property [Remote Desktop Services],ITsSbEnvironment interface, get_Name, sbtsv/ITsSbEnvironment::Name, sbtsv/ITsSbEnvironment::get_Name, termserv.itssbenvironment_name
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITsSbEnvironment::get_Name
 - sbtsv/ITsSbEnvironment::get_Name
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbEnvironment.Name
 - ITsSbEnvironment.get_Name
---

# ITsSbEnvironment::get_Name


## -description

Retrieves a value that indicates the name of the environment that hosts the target computer.

This property is read-only.

## -parameters

## -remarks

This method returns a string that is not directly used by Remote Desktop Connection Broker (RD Connection Broker). RD Connection Broker passes this string to resource plug-ins.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment">ITsSbEnvironment</a>