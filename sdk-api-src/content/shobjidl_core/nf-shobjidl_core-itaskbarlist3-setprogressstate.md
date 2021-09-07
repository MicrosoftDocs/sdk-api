---
UID: NF:shobjidl_core.ITaskbarList3.SetProgressState
title: ITaskbarList3::SetProgressState (shobjidl_core.h)
description: Sets the type and state of the progress indicator displayed on a taskbar button.
helpviewer_keywords: ["ITaskbarList3 interface [Windows Shell]","SetProgressState method","ITaskbarList3.SetProgressState","ITaskbarList3::SetProgressState","SetProgressState","SetProgressState method [Windows Shell]","SetProgressState method [Windows Shell]","ITaskbarList3 interface","TBPF_ERROR","TBPF_INDETERMINATE","TBPF_NOPROGRESS","TBPF_NORMAL","TBPF_PAUSED","_shell_ITaskbarList3_SetProgressState","shell.ITaskbarList3_SetProgressState","shobjidl_core/ITaskbarList3::SetProgressState"]
old-location: shell\ITaskbarList3_SetProgressState.htm
tech.root: shell
ms.assetid: ffa5566c-a6ad-4e96-a009-1e2006359f87
ms.date: 12/05/2018
ms.keywords: ITaskbarList3 interface [Windows Shell],SetProgressState method, ITaskbarList3.SetProgressState, ITaskbarList3::SetProgressState, SetProgressState, SetProgressState method [Windows Shell], SetProgressState method [Windows Shell],ITaskbarList3 interface, TBPF_ERROR, TBPF_INDETERMINATE, TBPF_NOPROGRESS, TBPF_NORMAL, TBPF_PAUSED, _shell_ITaskbarList3_SetProgressState, shell.ITaskbarList3_SetProgressState, shobjidl_core/ITaskbarList3::SetProgressState
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITaskbarList3::SetProgressState
 - shobjidl_core/ITaskbarList3::SetProgressState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Explorerframe.dll
api_name:
 - ITaskbarList3.SetProgressState
---

# ITaskbarList3::SetProgressState


## -description

Sets the type and state of the progress indicator displayed on a taskbar button.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

The handle of the window in which the progress of an operation is being shown. This window's associated taskbar button will display the progress bar.

### -param tbpFlags [in]

Type: <b>TBPFLAG</b>

Flags that control the current state of the progress button. Specify only one of the following flags; all states are mutually exclusive of all others.



#### TBPF_NOPROGRESS (0x00000000)

Stops displaying progress and returns the button to its normal state. Call this method with this flag to dismiss the progress bar when the operation is complete or canceled.



#### TBPF_INDETERMINATE (0x00000001)

The progress indicator does not grow in size, but cycles repeatedly along the length of the taskbar button. This indicates activity without specifying what proportion of the progress is complete. Progress is taking place, but there is no prediction as to how long the operation will take.



#### TBPF_NORMAL (0x00000002)

The progress indicator grows in size from left to right in proportion to the estimated amount of the operation completed. This is a determinate progress indicator; a prediction is being made as to the duration of the operation.



#### TBPF_ERROR (0x00000004)

The progress indicator turns red to show that an error has occurred in one of the windows that is broadcasting progress. This is a determinate state. If the progress indicator is in the indeterminate state, it switches to a red determinate display of a generic percentage not indicative of actual progress.



#### TBPF_PAUSED (0x00000008)

The progress indicator turns yellow to show that progress is currently stopped in one of the windows but can be resumed by the user. No error condition exists and nothing is preventing the progress from continuing. This is a determinate state. If the progress indicator is in the indeterminate state, it switches to a yellow determinate display of a generic percentage not indicative of actual progress.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Progress bar information is not shown in high contrast color schemes to guarantee that no accessibility needs are compromised.

Developers accustomed to the existing <a href="/windows/desktop/Controls/progress-bar-control-reference">progress bar</a> control should find the taskbar button progress indicator to be a similar experience both in concept and visuals. Here, the taskbar button itself becomes a progress bar. A taskbar button's progress indicator should be a reflection of a more detailed progress bar in the associated window. This allows the user to see specifics, such as the percentage number and the amount of time remaining, that cannot be shown in a taskbar button. Also, because a taskbar button can show the progress of only a single window in a group, it allows the user to check the progress of individual windows. It also provides progress information to the user when the taskbar button cannot, such as in a high-contrast color scheme.

Note that a taskbar button progress bar is not intended for use with normally peripheral actions such as the loading of a webpage or the printing of a document. That type of progress should continue to be shown in a window's <a href="/windows/desktop/Controls/status-bar-reference">status bar</a>.

The progress indicator is displayed between the taskbar button's icon or text and the background. If progress is shown for both the active taskbar button and an inactive button, shading in the respective progress bars is such that the active button is still obvious to the user. Also, button functionality such as the display of thumbnails continues to work normally when the button is being used to display progress.

When exiting an error or paused state, call this method again with the <b>TBPF_NORMAL</b> or <b>TBPF_INDETERMINATE</b> flag to continue in the original state or <b>TBPF_NOPROGRESS</b> if the operation is canceled.

<h3><a id="How_the_Taskbar_Button_Chooses_the_Progress_Indicator_for_a_Group"></a><a id="how_the_taskbar_button_chooses_the_progress_indicator_for_a_group"></a><a id="HOW_THE_TASKBAR_BUTTON_CHOOSES_THE_PROGRESS_INDICATOR_FOR_A_GROUP"></a>How the Taskbar Button Chooses the Progress Indicator for a Group</h3>
The taskbar button can show a progress indicator for only one window at a time. This includes the situation where the taskbar button represents a group and more than one window in that group is broadcasting progress information. In that case, the taskbar button chooses its progress display based on state priority. State priority is shown in the following table with priority 1 being the highest.


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
 



Changing a window's state changes its priority in relation to other windows in the group which in turn might change which window in a group is used for the progress indicator in the taskbar button.

In the case of a priority collision between two windows that are broadcasting determinate progress, the window with the least progress is used.

Based on this priority, the indeterminate progress indicator can be displayed in the taskbar button only in these cases:
                
<ul>
<li>The taskbar button does not represent a group and the single window that it represents has set TBPF_INDETERMINATE.</li>
<li>The taskbar button represents a group, only one window in that group is broadcasting progress information, and that window has set <b>TBPF_INDETERMINATE</b>.</li>
<li>The taskbar button represents a group, multiple windows in that group are broadcasting progress information, and all of those windows have set <b>TBPF_INDETERMINATE</b>.</li>
</ul>


A determinate progress indicator can be displayed in these cases:
                    
<ul>
<li>The taskbar button does not represent a group and the single window that it represents is broadcasting determinate progress information.</li>
<li>The taskbar button represents a group, only one window in that group is broadcasting progress information, and that window is broadcasting determinate progress information.</li>
<li>The taskbar button represents a group, multiple windows in that group are broadcasting progress information, at least one of those windows is broadcasting determinate progress information, and no window has set <b>TBPF_ERROR</b> or <b>TBPF_PAUSED</b>.</li>
</ul>


Note that a call to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue">SetProgressValue</a> will switch a progress indicator currently in an indeterminate mode (<b>TBPF_INDETERMINATE</b>) to a normal (determinate) display and clear the <b>TBPF_INDETERMINATE</b> flag.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist">ITaskbarList</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist2">ITaskbarList2</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3">ITaskbarList3</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue">ITaskbarList3::SetProgressValue</a>



<a href="/windows/desktop/shell/taskbar-extensions">Taskbar Extensions</a>