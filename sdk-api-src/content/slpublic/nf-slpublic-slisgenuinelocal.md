---
UID: NF:slpublic.SLIsGenuineLocal
title: SLIsGenuineLocal function
author: windows-sdk-content
description: Checks whether the specified application is a genuine Windows installation.
old-location: security\slisgenuinelocal.htm
old-project: SecSLApi
ms.assetid: e1983777-13c1-4bf5-834d-471db3bfa0f6
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: SLIsGenuineLocal, SLIsGenuineLocal function [Security], security.slisgenuinelocal, slpublic/SLIsGenuineLocal
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: slpublic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SL_ACTIVATION_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Slwga.dll
api_name:
-	SLIsGenuineLocal
product: Windows
targetos: Windows
req.lib: Slwga.lib
req.dll: Slwga.dll
req.irql: 
req.product: Outlook Express 6.0
---

# SLIsGenuineLocal function


## -description


Checks whether the specified application is a genuine Windows installation.


## -parameters




### -param pAppId [in]

A pointer to an <b>SLID</b> structure that specifies the application to check.


### -param pGenuineState [out]

A pointer to a value of the <a href="https://msdn.microsoft.com/3be69be1-289c-466a-9271-5309fd1319fe">SL_GENUINE_STATE</a> enumeration that specifies the state of the installation.


### -param pUIOptions [in, out, optional]

A pointer to an <a href="https://msdn.microsoft.com/5e793f09-1d12-4b69-8ba6-6c45421df533">SL_NONGENUINE_UI_OPTIONS</a> structure that specifies a dialog box to display if the installation is not genuine. If the value of this parameter is <b>NULL</b>, no dialog box is displayed.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



This function checks the <b>Tampered</b> flag of the license associated with the specified application. If the license is not valid, or if the <b>Tampered</b> flag of the license is set, the installation is not considered valid.



