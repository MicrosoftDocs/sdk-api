---
UID: NF:mswmdm.IWMDMProgress3.End3
title: IWMDMProgress3::End3
author: windows-sdk-content
description: The End3 method is called by Windows Media Device Manager to indicate that an operation has finished.
old-location: wmdm\iwmdmprogress3_end3.htm
tech.root: WMDM
ms.assetid: fb09cfa8-1a96-412f-a97a-6cc1638b0c77
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: End3, End3 method [windows Media Device Manager], End3 method [windows Media Device Manager],IWMDMProgress3 interface, IWMDMProgress3 interface [windows Media Device Manager],End3 method, IWMDMProgress3.End3, IWMDMProgress3::End3, IWMDMProgress3End3, mswmdm/IWMDMProgress3::End3, wmdm.iwmdmprogress3_end3
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMProgress3.End3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMDMProgress3::End3


## -description



The <b>End3</b> method is called by Windows Media Device Manager to indicate that an operation has finished. This method extends <a href="https://msdn.microsoft.com/85265eb7-0702-4890-b6cb-b247296fe392">IWMDMProgress2::End2</a> by providing additional input parameters for the identification (ID) of the event and for a pointer to the context of the commands.




## -parameters




### -param EventId [in]

A <b>GUID</b> specifying the event that is ending. Possible values are shown in the following table.

<table>
<tr>
<th>Event
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>SCP_EVENTID_ACQSECURECLOCK</td>
<td>Windows Media Device Manager is acquiring a secure clock from server.</td>
</tr>
<tr>
<td>SCP_EVENTID_NEEDTOINDIV</td>
<td>The device is being individualized. This is not currently used.</td>
</tr>
<tr>
<td>SCP_EVENTID_DRMINFO</td>
<td>
This event ID is used to notify the application with the version DRM header found in the content for each file.

The OPAQUECOMMAND structure returned has the <b>guidCommand</b> member set to SCP_PARAMID_DRMVERSION.

In addition, the data specifies one of the following flags:

WMDM_SCP_DRMINFO_NOT_DRMPROTECTED

WMDM_SCP_DRMINFO_V1HEADER

WMDM_SCP_DRMINFO_V2HEADER

</td>
</tr>
<tr>
<td>EVENT_WMDM_CONTENT_TRANSFER</td>
<td>Content is being transferred to or from the device.</td>
</tr>
</table>
 


### -param hrCompletionCode [in]

<b>HRESULT</b> specifying the completion code of the operation that was in progress. The <i>hrCompletionCode</i> parameter is the return code of the operation that ended. This parameter can be any <b>HRESULT</b>, including standard COM error codes, Win32 error codes converted to <b>HRESULT</b>, or Windows Media Device Manager error codes.


### -param pContext [in, out]

Pointer to an <a href="https://msdn.microsoft.com/5b39cf07-2816-4615-a754-e3f0c57bf4ce">OPAQUECOMMAND</a> structure containing a command sent directly to the device without being handled by Windows Media Device Manager. This parameter is optional and can be <b>NULL</b>. The context structure is a way for the component to send any relevant data with the event to the application. The component sending this structure should define how the application can interpret this data structure.




## -returns



Windows Media Device Manager ignores any return code returned by the <b>End3</b> method because the current operation is finished or cancelled before this method is called.




## -remarks



The interface that owns the method that is implementing an operation calls <b>End3</b> when the operation defined by the method is completed.


#### Examples

The following C++ code shows an example implementation of <b>End3</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT End3(GUID  EventId, HRESULT  hrCompletionCode, OPAQUECOMMAND*  pContext)
{
    // TODO: Display the message "IWMDMProgress3::End3 called."
    return S_OK;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b4fc7714-a7d0-409f-a47c-4903bab883cc">Enabling Notifications</a>



<a href="https://msdn.microsoft.com/fc3a7031-ac1b-45cf-889b-2d40d50b347d">IWMDMProgress3 Interface</a>



<a href="https://msdn.microsoft.com/0edddd8c-8144-40dc-801c-eb8c899be249">IWMDMProgress::End</a>
 

 

