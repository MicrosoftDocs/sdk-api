---
UID: NF:shobjidl_core.ITaskbarList3.SetProgressValue
title: ITaskbarList3::SetProgressValue
author: windows-sdk-content
description: Displays or updates a progress bar hosted in a taskbar button to show the specific percentage completed of the full operation.
old-location: shell\ITaskbarList3_SetProgressValue.htm
tech.root: shell
ms.assetid: 98646a68-d505-4d9b-b0f9-efda3da77005
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: ITaskbarList3 interface [Windows Shell],SetProgressValue method, ITaskbarList3.SetProgressValue, ITaskbarList3::SetProgressValue, SetProgressValue, SetProgressValue method [Windows Shell], SetProgressValue method [Windows Shell],ITaskbarList3 interface, _shell_ITaskbarList3_SetProgressValue, shell.ITaskbarList3_SetProgressValue, shobjidl_core/ITaskbarList3::SetProgressValue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Explorerframe.lib
req.dll: Explorerframe.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Explorerframe.dll
api_name:
 - ITaskbarList3.SetProgressValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITaskbarList3::SetProgressValue


## -description


Displays or updates a progress bar hosted in a taskbar button to show the specific percentage completed of the full operation.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

The handle of the window whose associated taskbar button is being used as a progress indicator.


### -param ullCompleted [in]

Type: <b>ULONGLONG</b>

An application-defined value that indicates the proportion of the operation that has been completed at the time the method is called.


### -param ullTotal [in]

Type: <b>ULONGLONG</b>

An application-defined value that specifies the value <i>ullCompleted</i> will have when the operation is complete.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<h3><a id="Determinate_Progress_Bar_Lifecycle"></a><a id="determinate_progress_bar_lifecycle"></a><a id="DETERMINATE_PROGRESS_BAR_LIFECYCLE"></a>Determinate Progress Bar Lifecycle</h3>
An application first calls <b>SetProgressValue</b> to begin the display of a determinate progress bar, and then calls it again as needed to update the bar as the progress changes. When progress is complete, the application must call <a href="https://msdn.microsoft.com/ffa5566c-a6ad-4e96-a009-1e2006359f87">SetProgressState</a> with the TBPF_NOPROGRESS flag to dismiss the progress bar.

<h3><a id="How_the_Taskbar_Button_Chooses_the_Progress_Indicator_for_a_Group"></a><a id="how_the_taskbar_button_chooses_the_progress_indicator_for_a_group"></a><a id="HOW_THE_TASKBAR_BUTTON_CHOOSES_THE_PROGRESS_INDICATOR_FOR_A_GROUP"></a>How the Taskbar Button Chooses the Progress Indicator for a Group</h3>
The taskbar button can show a progress indicator for only one window at a time. When the taskbar button represents a group and more than one of the windows in that group are broadcasting progress information, the taskbar button chooses its progress display based on the following state priority.




<table class="clsStd">
<tr>
<th>Priority</th>
<th>State</th>
</tr>
<tr>
<td>1</td>
<td>TBPF_ERROR</td>
</tr>
<tr>
<td>2</td>
<td>TBPF_PAUSED</td>
</tr>
<tr>
<td>3</td>
<td>TBPF_NORMAL</td>
</tr>
<tr>
<td>4</td>
<td>TBPF_INDETERMINATE</td>
</tr>
</table>
 



Unless <a href="https://msdn.microsoft.com/ffa5566c-a6ad-4e96-a009-1e2006359f87">SetProgressState</a> has set a blocking state (TBPF_ERROR or TBPF_PAUSED) for the window, a call to <b>SetProgressValue</b> assumes the TBPF_NORMAL state even if it is not explicitly set. A call to <b>SetProgressValue</b> overrides and clears the TBPF_INDETERMINATE state.

In the case of a priority collision where two windows are broadcasting determinate progress, the window with the least progress is used.

Based on that priority, this determinate (specific percentage) progress indicator can be displayed in these cases:
    
                    <ul>
<li>The taskbar button does not represent a group and the single window that it represents is broadcasting determinate progress information through this method.</li>
<li>The taskbar button represents a group, only one window in that group is broadcasting progress information, and that window is broadcasting determinate progress information through this method.</li>
<li>The taskbar button represents a group, multiple windows in that group are broadcasting progress information, at least one of those windows is broadcasting progress information through this method, and none of those windows has set the <a href="https://msdn.microsoft.com/ffa5566c-a6ad-4e96-a009-1e2006359f87">TBPF_ERROR</a> or <b>TBPF_PAUSED</b> state.</li>
</ul>


If a window in the group has set <a href="https://msdn.microsoft.com/ffa5566c-a6ad-4e96-a009-1e2006359f87">TBPF_ERROR</a> or <b>TBPF_PAUSED</b>, that state will be used for the button display. However, you can still make calls to <b>SetProgressValue</b> on other, unblocked windows in the group to update their progress in the background.


#### Examples

Here is an example of how an application could use <a href="https://msdn.microsoft.com/a5eb4e5a-df17-4aca-96fb-d8475e266b92">ITaskbarList3</a> to display progress while it is performing operations.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT CMyApp::ShowProgressInTaskbar(HWND hwnd, __in ITaskbarList3 *pTL)
{
    // Set the progress state of the button to indeterminate while you calculate
    // the number of operations to be performed.
    HRESULT hr = pTL-&gt;SetProgressState(hwnd, TBPF_INDETERMINATE);

    // Calculate the number of operations to perform.
    int cTotalOperations = _CalculateNumberOfOperationsToPerform();

    for (int i=0; i &lt; cTotalOperations &amp;&amp; SUCCEEDED(hr); i++)
    {
        // Update the progress. This call to SetProgressValue cancels the
        // indeterminate state and puts the button into normal progress mode.
        pTL-&gt;SetProgressValue(hwnd, i, cTotalOperations);
       
        // Do whatever operation your application needs to perform.
        hr = _PerformOperation(i);
    }

    // Tell the button that progress no longer needs to be displayed.
    pTL-&gt;SetProgressState(hwnd, TBPF_NOPROGRESS);
    
    return hr;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/c63f5fe8-4a8f-4ca8-bd6a-7733110bbb38">ITaskbarList</a>



<a href="https://msdn.microsoft.com/8af23586-349f-4d21-98cb-0aaa27a586ff">ITaskbarList2</a>



<a href="https://msdn.microsoft.com/a5eb4e5a-df17-4aca-96fb-d8475e266b92">ITaskbarList3</a>



<a href="https://msdn.microsoft.com/ffa5566c-a6ad-4e96-a009-1e2006359f87">ITaskbarList3::SetProgressState</a>



<a href="https://msdn.microsoft.com/cbf2b07d-d67c-4755-888c-d40692d13cae">Taskbar Extensions</a>
 

 

