---
UID: NF:msvidctl.IMSVidCtl.put_DisplaySize
title: IMSVidCtl::put_DisplaySize
author: windows-sdk-content
description: The put_DisplaySize method specifies the display size.
old-location: mstv\imsvidctl_put_displaysize.htm
old-project: mstv
ms.assetid: 1771e66b-e5f3-44f5-a489-e57baaf5cf25
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],put_DisplaySize method, IMSVidCtl.put_DisplaySize, IMSVidCtl::put_DisplaySize, IMSVidCtlput_DisplaySize, mstv.imsvidctl_put_displaysize, msvidctl/IMSVidCtl::put_DisplaySize, put_DisplaySize, put_DisplaySize method [Microsoft TV Technologies], put_DisplaySize method [Microsoft TV Technologies],IMSVidCtl interface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msvidctl.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msvidctl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MSVidCtlStateList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msvidctl.h
api_name:
 - IMSVidCtl.put_DisplaySize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidCtl::put_DisplaySize


## -description


The <b>put_DisplaySize</b> method specifies the display size.


## -parameters




### -param NewValue [in]

Specifies the display size as a member of the <a href="https://msdn.microsoft.com/2e939cbc-fc75-41d7-9fcb-32da5173f9bc">DisplaySizeList</a> enumeration.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



Setting this property has no effect if the <b>AutoSize</b> property is false.




## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>



<a href="https://msdn.microsoft.com/f3d5ed73-4781-46fb-8df4-a7dc339b755c">IMSVidCtl::get_DisplaySize</a>



<a href="https://msdn.microsoft.com/eb5863e2-380b-4bee-ac18-e5f28551a6ab">IMSVidCtl::put_AutoSize</a>
 

 

