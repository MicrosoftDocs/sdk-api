---
UID: NF:shimgdata.IShellImageData.SetEncoderParams
title: IShellImageData::SetEncoderParams
author: windows-sdk-content
description: Sets encoder parameters.
old-location: shell\IShellImageData_SetEncoderParams.htm
tech.root: shell
ms.assetid: 20a5b0ab-5dcb-4ea9-9c15-d7c1e6c2c6be
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: IShellImageData interface [Windows Shell],SetEncoderParams method, IShellImageData.SetEncoderParams, IShellImageData::SetEncoderParams, SetEncoderParams, SetEncoderParams method [Windows Shell], SetEncoderParams method [Windows Shell],IShellImageData interface, _shell_IShellImageData_SetEncoderParams, shell.IShellImageData_SetEncoderParams, shimgdata/IShellImageData::SetEncoderParams
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shimgdata.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shimgdata.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellImageData.SetEncoderParams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellImageData::SetEncoderParams


## -description


Sets encoder parameters.


## -parameters




### -param pbagEnc [in]

Type: <b><a href="https://msdn.microsoft.com/library/Aa768196(v=VS.85).aspx">IPropertyBag</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/library/Aa768196(v=VS.85).aspx">IPropertyBag</a> containing the encoder properties.


## -returns



Type: <b>HRESULT</b>

Always returns<b> S_OK</b>.




## -remarks



The <a href="https://msdn.microsoft.com/library/Aa768196(v=VS.85).aspx">IPropertyBag</a> passed in <i>pbagEnc</i> is used during a save operation. The image and any edits made to it, such as <a href="https://msdn.microsoft.com/42fd8596-e130-4029-bf3c-67199e8dd804">Rotate</a> or <a href="https://msdn.microsoft.com/ebcc9cc1-b6ee-4fb9-9125-54d6a9ee9434">Scale</a>, can be saved by calling <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> for either <a href="https://msdn.microsoft.com/7d34507f-8a16-43b4-8225-010798abc546">IPersistFile</a> or <a href="https://msdn.microsoft.com/97ea64ee-d950-4872-add6-1f532a6eb33f">IPersistStream</a> and calling their <b>Save</b> method.



