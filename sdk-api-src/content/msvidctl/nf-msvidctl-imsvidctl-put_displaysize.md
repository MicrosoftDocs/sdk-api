---
UID: NF:msvidctl.IMSVidCtl.put_DisplaySize
title: IMSVidCtl::put_DisplaySize (msvidctl.h)
author: windows-sdk-content
description: The put_DisplaySize method specifies the display size.
old-location: mstv\imsvidctl_put_displaysize.htm
tech.root: mstv
ms.assetid: 1771e66b-e5f3-44f5-a489-e57baaf5cf25
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],put_DisplaySize method, IMSVidCtl.put_DisplaySize, IMSVidCtl::put_DisplaySize, IMSVidCtlput_DisplaySize, mstv.imsvidctl_put_displaysize, msvidctl/IMSVidCtl::put_DisplaySize, put_DisplaySize, put_DisplaySize method [Microsoft TV Technologies], put_DisplaySize method [Microsoft TV Technologies],IMSVidCtl interface
ms.topic: method
f1_keywords: 
 - "msvidctl/IMSVidCtl.put_DisplaySize"
req.header: msvidctl.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidCtl::put_DisplaySize


## -description


The <b>put_DisplaySize</b> method specifies the display size.


## -parameters




### -param NewValue [in]

Specifies the display size as a member of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/ne-msvidctl-displaysizelist">DisplaySizeList</a> enumeration.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



Setting this property has no effect if the <b>AutoSize</b> property is false.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_displaysize">IMSVidCtl::get_DisplaySize</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-put_autosize">IMSVidCtl::put_AutoSize</a>
 

 

