---
UID: NF:xamlom.IXamlDiagnostics.GetHandleFromIInspectable
title: IXamlDiagnostics::GetHandleFromIInspectable
author: windows-sdk-content
description: Gets an InstanceHandle representation of an IInspectable.
old-location: xaml_diagnostics\ixamldiagnostics_gethandlefromiinspectable.htm
old-project: xaml_diagnostics
ms.assetid: 334497D9-11ED-4002-AEAB-0454EB62E53C
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetHandleFromIInspectable, GetHandleFromIInspectable method, GetHandleFromIInspectable method,IXamlDiagnostics interface, IXamlDiagnostics interface,GetHandleFromIInspectable method, IXamlDiagnostics.GetHandleFromIInspectable, IXamlDiagnostics::GetHandleFromIInspectable, xaml_diagnostics.ixamldiagnostics_gethandlefromiinspectable, xamlom/IXamlDiagnostics::GetHandleFromIInspectable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xamlom.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XamlOM.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VisualMutationType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xamlom.h
api_name:
 - IXamlDiagnostics.GetHandleFromIInspectable
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXamlDiagnostics::GetHandleFromIInspectable


## -description


Gets an <b>InstanceHandle</b> representation of an <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>.


## -parameters




### -param pInstance [in]

An instance of the object as an <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>.


### -param pHandle [out, retval]

A handle to the object.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1BCE3EC3-8B48-4F16-8E91-78776C07F309">IXamlDiagnostics</a>
 

 

