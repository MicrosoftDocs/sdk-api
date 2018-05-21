---
UID: NF:shobjidl_core.IFileDialog.ClearClientData
title: IFileDialog::ClearClientData
author: windows-driver-content
description: Instructs the dialog to clear all persisted state information.
old-location: shell\IFileDialog_ClearClientData.htm
old-project: shell
ms.assetid: bedb6fc8-7db7-4d29-a223-a9997b57c8a3
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: ClearClientData, ClearClientData method [Windows Shell], ClearClientData method [Windows Shell],IFileDialog interface, IFileDialog interface [Windows Shell],ClearClientData method, IFileDialog.ClearClientData, IFileDialog::ClearClientData, shell.IFileDialog_ClearClientData, shell_IFileDialog_ClearClientData, shobjidl_core/IFileDialog::ClearClientData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IFileDialog.ClearClientData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileDialog::ClearClientData


## -description


Instructs the dialog to clear all persisted state information.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Persisted information can be associated with an application or a GUID. If a GUID was set by using <a href="https://msdn.microsoft.com/2ab7d8bb-068d-4c5b-b273-68c7fc4f9956">IFileDialog::SetClientGuid</a>, that GUID is used to clear persisted information.



