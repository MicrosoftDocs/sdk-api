---
UID: NF:casetup.ICertSrvSetup.GetSupportedCATypes
title: ICertSrvSetup::GetSupportedCATypes
author: windows-sdk-content
description: Gets the types of certification authorities (CAs) that can be installed on a computer under the caller context.
old-location: security\icertsrvsetup_getsupportedcatypes.htm
old-project: seccrypto
ms.assetid: 404e5c34-f614-4555-9062-c28d4aac5c4b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetSupportedCATypes, GetSupportedCATypes method [Security], GetSupportedCATypes method [Security],ICertSrvSetup interface, ICertSrvSetup interface [Security],GetSupportedCATypes method, ICertSrvSetup.GetSupportedCATypes, ICertSrvSetup::GetSupportedCATypes, casetup/ICertSrvSetup::GetSupportedCATypes, security.icertsrvsetup_getsupportedcatypes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: casetup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Casetup.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CEPSetupProperty
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certocm.dll
api_name:
 - ICertSrvSetup.GetSupportedCATypes
product: Windows
targetos: Windows
req.lib: 
req.dll: Certocm.dll
req.irql: 
---

# ICertSrvSetup::GetSupportedCATypes


## -description


The <b>GetSupportedCATypes</b> method gets the types of <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authorities</a> (CAs) that can be installed on a computer under the caller context. This method does not change the state of the <b>CCertSrvSetup</b> object.


## -parameters




### -param pCATypes [out]

A pointer to a <b>VARIANT</b> array of <b>VT_UI4</b> types that specify the supported CAs. The <a href="https://msdn.microsoft.com/32b20317-c0ef-4896-a8c6-309e34f87c30">ENUM_CATYPES</a> enumeration specifies the possible values for the array.


## -see-also




<a href="https://msdn.microsoft.com/6792a0d6-d304-481d-a97b-5fb7033c7eae">ICertSrvSetup</a>
 

 

