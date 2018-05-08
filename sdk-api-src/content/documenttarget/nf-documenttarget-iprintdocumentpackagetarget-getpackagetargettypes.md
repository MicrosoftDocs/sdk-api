---
UID: NF:documenttarget.IPrintDocumentPackageTarget.GetPackageTargetTypes
title: IPrintDocumentPackageTarget::GetPackageTargetTypes
author: windows-driver-content
description: Enumerates the supported target types.
old-location: xps\iprintdocumentpackagetarget_getpackagetargettypes.htm
old-project: printdocs
ms.assetid: 2875B751-0D49-4CFC-AF96-7009400E5D6E
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetPackageTargetTypes, GetPackageTargetTypes method [XPS Documents and Packaging], GetPackageTargetTypes method [XPS Documents and Packaging],IPrintDocumentPackageTarget interface, IPrintDocumentPackageTarget interface [XPS Documents and Packaging],GetPackageTargetTypes method, IPrintDocumentPackageTarget.GetPackageTargetTypes, IPrintDocumentPackageTarget::GetPackageTargetTypes, documenttarget/IPrintDocumentPackageTarget::GetPackageTargetTypes, xps.iprintdocumentpackagetarget_getpackagetargettypes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: documenttarget.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PrintDocumentPackageCompletion
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Documenttarget.h
api_name:
-	IPrintDocumentPackageTarget.GetPackageTargetTypes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IPrintDocumentPackageTarget::GetPackageTargetTypes


## -description


Enumerates the supported target types.


## -parameters




### -param targetCount [out]

The number of supported target types.


### -param targetTypes [out]

The array of supported target types. An array of GUIDs.


## -returns



If the <b>GetPackageTargetTypes</b> method completes successfully, it returns an S_OK. Otherwise it returns the appropriate HRESULT error code.




## -remarks



In the case of a multi-format driver, the first GUID returned in the <i>targetTypes</i> array is the XPS format preferred by the driver.




## -see-also




<a href="https://msdn.microsoft.com/0F63C626-DB58-4952-BBB3-7E3901429C35">IPrintDocumentPackageTarget</a>
 

 

